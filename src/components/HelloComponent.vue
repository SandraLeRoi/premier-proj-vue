<template>
  <div>
    <h1>{{ message }}</h1>
    <input type="text" v-model="name">
  </div>
</template>

<script>
export default {
  name: "HelloComponent",
  data() {
    return {
      name: ""
    }
  },
  computed: {
    message() {
      if(this.name) {
        return "Bonjour" + this.name
      }
    }
  }
}
</script>

<style scoped>

</style>