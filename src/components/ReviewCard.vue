<template>
  <div class="review-container">
    <div class="user">
      <img :src="review.user.images.jpg.image_url" alt="User Avatar">
      <h3>{{ review.user.username }}</h3>
      <a :href="review.user.url" target="_blank">Профиль</a>
    </div>
    <div class="content">
      <h1 v-if="review.is_spoiler "> Имеется спойлер! </h1>
      <p>Обзор: {{ review.review }}</p>
      <p>Дата: {{ review.date }}</p>
      <p>Оценка: {{ review.score }}</p>
      <p>Теги: {{ review.tags.join(", ") }}</p>
      <p>Просмотренно серий: {{ review.episodes_watched }}</p>
      <p>Тип: {{ review.type }}</p>
      <p>Общие реакции: {{ review.reactions.overall }}</p>
    </div>
  </div>
</template>
<script lang="ts">

export default {
  props: ['review'],
  name: 'ReviewCard'
}
</script>

<style scoped>
.review-container {
display: flex;
padding: 10px 20px;
text-align: justify;
width: 100%;
}

img {
width: 225px;
margin-right: 20px;
border-radius: 10px;
}

svg {
width: 24px;
height: 24px;
}

a {
text-decoration: none;
}

h1 {
  color: red;
}

.title {
font-size: 28px;
}

.rating {
display: flex;
align-items: center;
gap: 5px;
fill: black;
}

.score {
font-size: 24px;
}

.synopsis {
color: #a4a4a4;
font-size: 16px;
font-weight: 300;
}

.info {
display: flex;
flex-direction: column;
justify-content: flex-start;
align-items: flex-start;
gap: 10px;
}

@media screen and (max-width: 768px) {
img {
  width: 33%;
}

.title {
  font-size: 16px;
}

.info {
  gap: 3px
}

svg {
  width: 14px;
  height: 14px;
}

.score {
  font-size: 14px;
}

.synopsis {
  font-size: 8px;
  display: -webkit-box;
  -webkit-line-clamp: 4;
  -webkit-box-orient: vertical;
  overflow: hidden;
}

.episodes {
  font-size: 10px;
}
}
</style>
