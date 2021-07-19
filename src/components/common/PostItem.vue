<template>
  <div class="post">
    <div class="post__intro">
      <UserCard :username="username" :avatar="avatar"></UserCard>
    </div>
    <div class="post__main">
      <div class="post__title">
        {{ title }}
      </div>
      <div class="post__text">
        {{ text }}
      </div>
      <div class="post__git-wrapper">
        <GitPlugin :star="star" :fork="fork"></GitPlugin>
      </div>
    </div>
    <div class="post__issues">
      <Issues @onToggle="toggle"></Issues>
      <ul class="post__issues-list" v-if="show">
        <li class="post__issues-item">
          <div class="post__issues-name">joshua_l</div>
          <div class="post__issues-text">Enable performance measuring in production, at the user's request</div>
        </li>
        <li class="post__issues-item">
          <div class="post__issues-name">joshua_l</div>
          <div class="post__issues-text">Enable performance measuring in production, at the user's request</div>
        </li>
        <li class="post__issues-item">
          <div class="post__issues-name">joshua_l</div>
          <div class="post__issues-text">Enable performance measuring in production, at the user's request</div>
        </li>
      </ul>
    </div>
    <div class="post__date">15 may</div>
  </div>
</template>

<script>
import UserCard from './UserCard.vue'
import Issues from './Issues.vue'
import { GitPlugin } from './GitPlugin'
export default {
  name: 'PostItem',
  components: {
    UserCard,
    Issues,
    GitPlugin
  },
  data () {
    return {
      show: false
    }
  },
  props: {
    title: String,
    text: String,
    avatar: String,
    username: String,
    star: String,
    fork: String
  },
  methods: {
    toggle (isOpen) {
      this.show = isOpen
    }
  }
}
</script>
<style scoped>
.post__intro{
  margin-bottom: 16px;
}

.post__date{
  margin-top: 10px;
  font-style: normal;
  font-weight: normal;
  font-size: 12px;
  line-height: 14px;
  /* or 117% */

  display: flex;
  align-items: center;
  letter-spacing: 0.1em;
  text-transform: uppercase;

  color: rgba(0, 0, 0, 0.4);
}

.post__title{
  font-style: normal;
  font-weight: bold;
  font-size: 26px;
  line-height: 28px;
  color: #292929;
  margin-bottom: 16px;
}

.post__text{
  font-style: normal;
  font-size: 14px;
  line-height: 160%;
  color: #404040;
}

.post__main{
  background: #FFFFFF;
  border: 1px solid #F1F1F1;
  box-shadow: 0px 4px 40px rgba(0, 0, 0, 0.07);
  border-radius: 10px;
  padding: 24px 20px;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.post__issues-list{
  margin-top: 10px;
}

.post__issues{
  margin-top: 18px;
}
.post__issues-item{
  display: flex;
  margin-bottom: 8px;
}
.post__issues-name{
  font-weight: bold;
  margin-right: 8px;
}
.post__git-wrapper{
  margin-top: 32px;
}
</style>
