<template>
  <div class="container">
    <img :src="manga.images.jpg.large_image_url" alt="">
    <div class="info">
      <router-link :to="{ name: 'manga', params: { id: manga.mal_id } }">
        <h1>{{ manga.title }}</h1>
      </router-link>
      <div class="rating"><svg viewBox="0 0 64 64" version="1.1" xmlns="http://www.w3.org/2000/svg"
          xmlns:xlink="http://www.w3.org/1999/xlink" xml:space="preserve" xmlns:serif="http://www.serif.com/"
          style="fill-rule:evenodd;clip-rule:evenodd;stroke-linejoin:round;stroke-miterlimit:2;" stroke="#ffffff">
          <g id="SVGRepo_bgCarrier" stroke-width="0"></g>
          <g id="SVGRepo_tracerCarrier" stroke-linecap="round" stroke-linejoin="round"></g>
          <g id="SVGRepo_iconCarrier">
            <rect id="Icons" x="-512" y="-192" width="1280" height="800" style="fill:none;"></rect>
            <g id="Icons1" serif:id="Icons">
              <g id="Strike"> </g>
              <g id="H1"> </g>
              <g id="H2"> </g>
              <g id="H3"> </g>
              <g id="list-ul"> </g>
              <g id="hamburger-1"> </g>
              <g id="hamburger-2"> </g>
              <g id="list-ol"> </g>
              <g id="list-task"> </g>
              <g id="trash"> </g>
              <g id="vertical-menu"> </g>
              <g id="horizontal-menu"> </g>
              <g id="sidebar-2"> </g>
              <g id="Pen"> </g>
              <g id="Pen1" serif:id="Pen"> </g>
              <g id="clock"> </g>
              <g id="external-link"> </g>
              <g id="hr"> </g>
              <g id="info"> </g>
              <g id="warning"> </g>
              <g id="plus-circle"> </g>
              <g id="minus-circle"> </g>
              <g id="vue"> </g>
              <g id="cog"> </g>
              <g id="logo"> </g>
              <path id="star"
                d="M32.001,9.188l5.666,17.438l18.335,0l-14.833,10.777l5.666,17.438l-14.834,-10.777l-14.833,10.777l5.666,-17.438l-14.834,-10.777l18.335,0l5.666,-17.438Z">
              </path>
              <g id="radio-check"> </g>
              <g id="eye-slash"> </g>
              <g id="eye"> </g>
              <g id="toggle-off"> </g>
              <g id="shredder"> </g>
              <g id="spinner--loading--dots-" serif:id="spinner [loading, dots]"> </g>
              <g id="react"> </g>
              <g id="check-selected"> </g>
              <g id="turn-off"> </g>
              <g id="code-block"> </g>
              <g id="user"> </g>
              <g id="coffee-bean"> </g>
              <g id="coffee-beans">
                <g id="coffee-bean1" serif:id="coffee-bean"> </g>
              </g>
              <g id="coffee-bean-filled"> </g>
              <g id="coffee-beans-filled">
                <g id="coffee-bean2" serif:id="coffee-bean"> </g>
              </g>
              <g id="clipboard"> </g>
              <g id="clipboard-paste"> </g>
              <g id="clipboard-copy"> </g>
              <g id="Layer1"> </g>
            </g>
          </g>
        </svg>
        <span class="score">{{ manga.score }}</span>
      </div>
      <p class="synopsis">{{ manga.synopsis }}</p>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue"

export default defineComponent({
  props: ['manga']
})
</script>
<style scoped>
.container {
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

.title {
  font-size: 28px;
}

.rating {
  display: flex;
  align-items: center;
  gap: 5px;
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
}</style>