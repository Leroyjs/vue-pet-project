<template>
  <header class="header main-padding">
    <div class="header__inner">
      <a href="/" class="header__logo-wrapper">
        <img src="../../../media/gitogram-logo.svg" alt="gitogram" class="header__logo">
      </a>
      <div class="header__links-wrapper">
        <a href="" class="header__link">
          <Icon name="home"></Icon>
        </a>
        <a href="" class="header__link">
          <img src="../../../media/ProfilePic.jpg" alt="" class="header__link-inner header__link-inner_profile-img">
        </a>
        <a href="" class="header__link">
          <Icon name="logout"></Icon>
        </a>
      </div>
    </div>
    <slot name="content"></slot>
  </header>
</template>

<script>
import { Icon } from '../../../icons'
export default {
  name: 'Header',
  components: { Icon }
}
</script>

<style src='./style.scss' lang='scss' scoped>

</style>
