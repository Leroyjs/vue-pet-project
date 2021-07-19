<template>
  <div class="user-card">
    <img :src="avatar" alt="" class="user-card__img">
    <div class="user-card__name">{{ username }}</div>
  </div>
</template>

<script>
export default {
  name: 'UserCard',
  props: {
    avatar: String,
    username: String
  }
}
</script>
<style scoped>
.user-card{
  display: flex;
  align-items: center;
}
.user-card__img{
  width: 44px;
  height: 44px;
  border-radius: 50%;
  margin-right: 14px;
}
.user-card__name{
  font-style: normal;
  font-weight: bold;
  font-size: 18px;
  line-height: 18px;
  /* identical to box height, or 100% */

  letter-spacing: -0.1px;

  /* add */

  color: #262626;
}
</style>
