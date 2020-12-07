<template>
  <div>
    <h1>{{message}}</h1>
    <button @click="add">+</button>
    <button @click="less">-</button>
    <h1>{{compteur}}</h1>
    <!-- <input type="number" :value="counter" @input="updateCounter"> -->
    <input type="number" v-model="counter">
    <button @click="addTask">Ajouter une tache</button>
    <div :key="index" class="task" v-for="(task, index) in tasks">
      <h1>{{ task }}</h1>
    </div>

  </div>
</template>

<script>
import HelloWorld from "@/components/HelloWorld.vue";
export default {
name: "Counter",
  data() {
    return {
      compteur: 0,
      tasks: [
          "Commander un kebab",
          "finir mon cours de Vue",
          "essayer de finir Skyrim"
      ]
    }
  },
  props: {
    message: {
      type: String,
      default: "compteur"
    },
  },
  methods: {
    add() {
      this.compteur++
    },
    less() {
      this.compteur = this.compteur - 1
    },
    updateCounter(event){
      this.compteur = parseInt(event.target.value);
    },
    addTask() {
      this.tasks.push('New task')
    }
  },
  components: {
    HelloWorld
  },

}
</script>

<style scoped>

</style>