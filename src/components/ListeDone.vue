<template>
    <div>
        <!-- composant done -->
   <button v-on:click="$emit('changeColor',index)">-Done-</button>
  <!--fin conposant done -->
    </div>
</template>
<script>
export default {
    name: "liste-done",
    props: {
        index: Number
    }
}
</script>