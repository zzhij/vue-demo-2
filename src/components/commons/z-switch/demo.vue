<template>
  <div class="zswitch-demo">
    <z-switch v-model="switchValue"></z-switch>
  </div>
</template>

<script>
import ZSwitch from './ZSwitch'
export default {
  data () {
    return {
      switchValue: true
    }
  },
  components: {
    ZSwitch
  }
}
</script>

<style>

</style>
