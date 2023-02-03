<template>
  <div class="screen">
    <h1>Interact Components here...</h1>
    <CardFace
      v-for="(card, index) in cardsContext"
      :key="index"
      :imgBackFaceUrl="`images/${card}.png`"
    />
  </div>
</template>
<script>
import CardFace from "./CardFace.vue";
export default {
  props: {
    cardsContext: {
      type: Array,
      default: function () {
        return [];
      },
    },
  },
  components: {
    CardFace,
  },
};
</script>
