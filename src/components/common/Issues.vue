<template>
  <div class="issues">
    <div class="issues__inner" @click="toggle">
      <div class="issues__text">{{isOpen ? 'Hide': 'Show'}} issues</div>
      <img src="../../media/arrow-top.svg" alt="" :class="['issues__arrow', {issues__arrow_active:!isOpen}]">
    </div>
  </div>
</template>

<script>
export default {
  name: 'Issues',
  data () {
    return {
      isOpen: false
    }
  },
  methods: {
    toggle () {
      this.isOpen = !this.isOpen
      this.$emit('onToggle', this.isOpen)
    }
  }
}
</script>
<style scoped>
.issues__inner{
  display: flex;
  align-items: center;
  cursor: pointer;
}
.issues__text{
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 160%;
  color: #292929;
  margin-right: 5px;
}
.issues__arrow_active{
  transform: rotate(180deg);
}
</style>
