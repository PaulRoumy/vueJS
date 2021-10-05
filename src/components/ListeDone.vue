<template>
    <div>
        <!-- composant done -->
   <button v-on:click="this.$emit('color')">-Done-</button>
  <!--fin conposant done -->
    </div>
</template>
<script>
export default {
    name: "liste-done"
}
</script>