<template>
  <ul class="header-user-list">
    <li class="header-user-list__item-wrapper" v-for="story in stories" :key="story.id">
      <div class="header-user-list__img-wrapper">
        <img :src="story.avatar" alt="" class="header-user-list__item">
      </div>
      <div class="header-user-list__item-text">{{story.username}}</div>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'HeaderUserList',
  props: {
    stories: {
      type: Array,
      required: true
    }
  }
}
</script>

<style scoped src='./styles.scss' lang='scss'></style>
