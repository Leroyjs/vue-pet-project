<template>
  <div class="git-plugin">
    <button class="git-plugin__button">
      <div class="git-plugin__icon">
        <Icon name="star"></Icon>
      </div>
      star
    </button>
    <div class="git-plugin__count">
      {{star}}
    </div>
    <button class="git-plugin__button git-plugin__button_fork">
      <div class="git-plugin__icon">
        <Icon name="fork"></Icon>
      </div>
      fork
    </button>
    <div class="git-plugin__count">
      {{fork}}
    </div>
  </div>
</template>

<script>
import { Icon } from '../../../icons'
export default {
  name: 'GitPugin',
  components: { Icon },
  props: {
    star: String,
    fork: String
  }
}
</script>

<style src="./style.scss" lang="scss" scoped>

</style>
