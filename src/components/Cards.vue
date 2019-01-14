<template>
  <div
    style="height: 500px; width: 500px; border: 1px solid red; position: relative;"
  >
    <!-- render this with a for loop -->
    <vue-draggable-resizable
      :grid="[10, 10]"
      :w="100"
      :h="100"
      v-on:dragging="onDrag"
      v-on:resizing="onResize"
      :parent="true"
      :resizable="false"
    >
    </vue-draggable-resizable>
  </div>
</template>

<script>
import VueDraggableResizable from "vue-draggable-resizable";

export default {
  name: "cards",
  components: {
    VueDraggableResizable
  },
  data() {
    return {
      width: 0,
      height: 0,
      x: 0,
      y: 0
    };
  },
  methods: {
    onResize: function(x, y, width, height) {
      this.x = x;
      this.y = y;
      this.width = width;
      this.height = height;
    },
    onDrag: function(x, y) {
      this.x = x;
      this.y = y;
    }
  }
};
</script>

<style></style>
