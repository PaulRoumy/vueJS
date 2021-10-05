<template>
  <span v-bind:style="{ color: item.activeColor }">
    {{ item.task }}
  </span>
  
</template>






<script>
export default {
  name: "liste-item",
  props: {
    item: Object,
  },
  created:{
    
  }
};
</script>
