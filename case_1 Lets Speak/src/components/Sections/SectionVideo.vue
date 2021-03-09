<template>
  <section class="video">
    <video
      class="lesson-video"
      poster="https://assets.htmlacademy.ru/content/skills/6/case-01/img/image-18.jpg"
      width="540"
      height="300"
    >
      <source src="video.mp4" type="video/mp4" />
    </video>
    <div class="video-play-list-wrapper box">
      <h3>Курс English A1</h3>
      <ul class="play-list">
        <li
          :class="'play-item ' + (video.isActive ? 'play-item-active' : '')"
          v-for="(video, key) of videoList"
          :key="key"
        >
          <button class="play-button" type="button"></button>
          <h4>{{ video.title }}</h4>
          <p>{{ video.descripion }}</p>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      videoList: [
        { title: 'Урок 8', descripion: 'Времена глаголов', isActive: false },
        { title: 'Урок 9', descripion: 'Неправильные глаголы', isActive: true },
        { title: 'Урок 10', descripion: 'Present Simple', isActive: false },
        { title: 'Урок 11', descripion: 'Past Simple', isActive: false }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
@import '../../style/base/colors';

.video {
  grid-area: video;
  display: grid;
  grid-template-columns: 2fr 1fr;
  grid-gap: 20px;

  h3 {
    margin: 20px 0 13px 30px;
    border-bottom: 1px solid #e4e8fc;
  }
}

.video-play-list-wrapper {
  position: relative;
  height: 300px;
  background: $primaryWhite;
  box-shadow: 0 1px 4px rgba(60, 66, 95, 0.2);
  border-radius: 4px;
}

.play-list {
  padding: 0;
  margin: 0;
  list-style: none;
  height: 235px;
  overflow-y: auto;
}

.lesson-video {
  width: 540px;
  height: 300px;
}
.play-item {
  display: grid;
  grid-template-columns: 32px auto;
  grid-template-rows: auto auto;
  grid-template-areas:
    'button title'
    'button desc';
  grid-column-gap: 13px;
  padding: 8px 10px 8px 30px;

  font-weight: 300;
  font-size: 14px;
  line-height: 16px;
  color: #3c425f;
  &-active {
    background-color: $lightBlue;

    .play-button {
      background-color: $indigo;
      &::before {
        border-left-color: $primaryWhite;
      }
    }
  }
  h4 {
    grid-area: title;
    margin: 0;
  }
  p {
    grid-area: desc;
    margin: 0;
  }
}
.play-button {
  position: relative;
  grid-area: button;
  width: 32px;
  height: 32px;
  background-color: $lightBlue;
  border-radius: 4px;
  border: none;
}

.play-button::before {
  content: '';
  position: absolute;
  width: 0;
  height: 0;
  left: 0;
  top: 0;
  transform: translate(12px, 10px);
  border-top: 6px solid transparent;
  border-left: 12px solid $darkBlue;
  border-bottom: 6px solid transparent;
  border-right: 12px solid transparent;
}
</style>