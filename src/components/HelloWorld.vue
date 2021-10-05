<template>
  <div class="liste">
    <h3>To-Do Liste</h3>
    <!-- composant liste -->
    <ul>
      <li v-for="(item, index) in items" :key="item.task">
        <!-- composant element -->
        <liste-item :item="item" />
        <liste-done :index="index" v-on:changeColor="changeColor(index)" />
      </li>
      <!-- fin composant element -->
    </ul>
    <input type="text" v-model="newItem" />
    <button type="submit" v-on:click="addTask">Ajouter</button>

    <!-- fin composant liste -->
  </div>
</template>

<script>
import ListeDone from "./ListeDone.vue";
import ListeItem from "./ListeItem.vue";

export default {
  components: { ListeItem, ListeDone },

  name: "HelloWorld",
  data() {
    return {
      items: [
        { task: "Pizza", activeColor: "red" },
        { task: "Phantom", activeColor: "red" },
      ],
      newItem: null,
    };
  },
  methods: {
    changeColor(index) {
      if (this.items[index].activeColor == "red") {
        this.items[index].activeColor = "green";
      } else if (this.items[index].activeColor == "green") {
        this.items[index].activeColor = "red";
      }
    },
    addTask() {
      this.items.push({ task: this.newItem, activeColor: "red" });
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

