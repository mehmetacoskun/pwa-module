<template>
  <main>
    <h1>Joshqun, Hello World</h1>
  </main>
</template>

<script>
export default {
  asyncData () {
    return {
      date: Date.now()
    }
  },
  computed: {
    computedDate () {
      return new Date(this.date)
    }
  },
  mounted () {
    this.int = setInterval(() => {
      this.date = Date.now()
    }, 1000)
  },
  beforeDestroy () {
    clearInterval(this.int)
  }
}
</script>

<style scoped>
.icon {
  max-width: 100%;
}
</style>
