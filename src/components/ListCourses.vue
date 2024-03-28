<template>
  <div class="main">
    <h1>Список курсов</h1>
    <div class="card" v-for="(item) in cards" :key="item.id">
      <div class="title">{{ item.title }}</div>
      <div class="description">{{ item.description }}</div>
      <div class="duration">{{ item.duration }}</div>
      <div class="isActive">
        <div v-if="item.isActive" class="card-is-active"></div>
        <div v-else class="card-is-not-active">Кажется, курс уже не существует...</div>
      </div>
    </div>
  </div>
</template>

<script setup>
import {ref} from 'vue'
    const cards = ref([
      {
        id: 1,
        title: "Python-разработчик",
        description: "Описание: На Python пишут сайты, приложения, игры и чат-боты. Netflix, Spotify, Google, Dropblox и Youtube написаны на Python.",
        duration: '10 месяцев',
        isActive: true,
      },
      {
        id: 2,
        title: "Графический дизайнер",
        description: "Описание: Научим делать бренды узнаваемыми через создание логотипов, графики для рекламы, упаковки и не только.",
        duration: '6 месяцев',
        isActive: true,
      },
      {
        id: 3,
        title: "Веб-разработчик",
        description: "Описание: Веб-разработчик создает сайты, сервисы и приложения, которыми мы ежедневно пользуемся.",
        duration: '7 месяцев',
        isActive: true,
      },
      {
        id: 4,
        title: "Инженер по тестированию",
        description: "Описание: Вы научитесь находить ошибки в работе сайтов и приложений с помощью Java, JavaScript или Python.",
        duration: '7 месяцев',
        isActive: true,
      },
      {
        id: 5,
        title: "",
        description: "",
        duration: '',
        isActive: false,
      },
      {
        id: 6,
        title: "",
        description: "",
        duration: '',
        isActive: false,
      },
      {
        id: 7,
        title: "",
        description: "",
        duration: '',
        isActive: false,
      },
    ])
</script>

<style scoped>

.card {
  padding: 10px;
  padding-left: 20px;
  width:450px;
  margin-top: 10px;
  margin-right: 15px;
  box-sizing: border-box;
  background: rgb(226, 226, 226);
  border-radius: 10px;
  display: inline-block;
  flex-wrap: wrap;
  align-content: center;
}

.title {
font-size: 18px;
font-weight: 600;
margin-bottom: 8px;
}

.description {
color: rgb(106, 109, 114);
margin-bottom: 16px;
}

.duration {
  color: black;
  margin-bottom: 16px;
  font-size: 18px;
}

.card-is-not-active {
color: rgb(255,0,255);
border-radius: 4px;
margin-bottom: 12px;
font-size: 18px;
}

.form {
margin-bottom: 12px;
}

input {
margin-left: 4px;
margin-bottom: 8px;
}

</style>
