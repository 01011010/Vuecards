<template>
  <div><!-- this is where the base shoul live, the moel for the card --></div>
</template>

<script>
import VueDraggableResizable from "vue-draggable-resizable";

export default {
  name: "card-base",
  components: {},
  data() {
    return {
      card: {
        title: "hw"
      }
    };
  },
  methods: {}
};
</script>

<style>
#card-base {
  background-color: gray;
}
</style>
