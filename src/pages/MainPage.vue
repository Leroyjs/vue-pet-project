<template>
  <Header>
    <template #content>
      <HeaderUserList v-if="stories.length" :stories="stories"/>
    </template>
  </Header>
  <div class="main-padding main-page__items-wrapper">
    <div class="post-wrapper" v-for="post in posts" :key="post.is">
      <PostItem :title="post.title" :text="post.text" :star="post.star" :fork="post.fork" :avatar="post.avatar" :username="post.username"/>
    </div>
  </div>
</template>

<script>
import { Header } from '../components/general/Header'
import { HeaderUserList } from '../components/common/HeaderUserList'
import PostItem from '../components/common/PostItem.vue'

export default {
  name: 'MainPage',
  components: {
    Header,
    PostItem,
    HeaderUserList
  },
  data () {
    return { stories, posts }
  }
}
const stories = [
  {
    id: '0',
    avatar: 'https://interactive-examples.mdn.mozilla.net/media/cc0-images/grapefruit-slice-332-332.jpg',
    username: 'some name'
  },
  {
    id: '1',
    avatar: 'https://interactive-examples.mdn.mozilla.net/media/cc0-images/grapefruit-slice-332-332.jpg',
    username: 'some name'
  }
]
const posts = [
  {
    id: '0',
    avatar: 'https://interactive-examples.mdn.mozilla.net/media/cc0-images/grapefruit-slice-332-332.jpg',
    username: 'some name',
    title: 'Vue.js',
    text: 'JavaScript framework for building interactive web applications ⚡',
    star: '12',
    fork: '1'
  },
  {
    id: '1',
    avatar: 'https://interactive-examples.mdn.mozilla.net/media/cc0-images/grapefruit-slice-332-332.jpg',
    username: 'some name',
    title: 'Vue.js',
    text: 'JavaScript framework for building interactive web applications ⚡',
    star: '12',
    fork: '1'
  }
]
</script>

<style scoped>
.post-wrapper {
  margin-top: 32px;
}
.main-page__items-wrapper {
  margin-bottom: 64px;
}
</style>
