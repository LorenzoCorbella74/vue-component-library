<template>
  <div class="background-special">
    <button @click="increment" class="global-btn">{{ text }}</button>
  </div>
</template>
<script>
export default {
  name:'SimpleComponent',
  data () {
    return {
      count: 0
    }
  },
  computed: {
    times () {
      return this.count > 1
        ? 'times'
        : 'time'
    },
    text () {
      return `I have been clicked ${this.count} ${this.times}`
    }
  },
  methods: {
    increment () {
      this.count += 1
    }
  }
}
</script>