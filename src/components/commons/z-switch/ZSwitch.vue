<template>
  <div class="switch-box">
    sdasd
    <div class="z-switch"
      @click="changeSwitch"
      role="switch"
      :class="{'s-switch--on': newSwitch}"
      :aria-checked="newSwitch">
      <div class="z-switch__node"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ZSwitch',
  model: {
    prop: 'modelValue',
    event: 'change'
  },
  props: {
    modelValue: {
      type: Boolean,
      default: false
    }
  },
  computed: {
    newSwitch () {
      return this.modelValue
    }
  },
  data () {
    return {}
  },
  methods: {
    changeSwitch () {
      this.$emit('change', !this.newSwitch)
    }
  }
}
</script>

<style scoped lang="scss">
.z-switch {
  position: relative;
  display: inline-block;
  box-sizing: content-box;
  width: 2em;
  height: 1em;
  font-size: 30px;
  background-color: #fff;
  border: 1px solid rgba(0, 0, 0, 0.1);
  border-radius: 1em;
  cursor: pointer;
  transition: background-color 0.3s;
  &.s-switch--on {
    background-color: #1989fa;
    .z-switch__node {
      transform: translateX(1em);
    }
  }
  .z-switch__node {
    top: 0;
    left: 0;
    width: 1em;
    height: 1em;
    background-color: #fff;
    border-radius: 100%;
    box-shadow: 0 3px 1px 0 rgba(0, 0, 0, 0.05), 0 2px 2px 0 rgba(0, 0, 0, 0.1), 0 3px 3px 0 rgba(0, 0, 0, 0.05);
    transition: transform 0.3s cubic-bezier(0.3, 1.05, 0.4, 1.05);
  }
}
</style>
