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
    <div class="video-play-list-wrapper">
      <ul class="play-list">
        <li class="play-item" v-for="(video, key) of videoList" :key="key">
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
        { title: "Урок 8", descripion: "Времена глаголов" },
        { title: "Урок 9", descripion: "Неправильные глаголы" },
        { title: "Урок 10", descripion: "Present Simple" },
        { title: "Урок 11", descripion: "Past Simple" },
      ],
    };
  },
};
</script>