<template>
  <div class="star-rating">
    <span v-for="(n, index) in max" :key="index">&star;</span>
    <div class="star-rating__current" :style="{ width: getRating + '%' }">
      <span v-for="(n, index) in max" :key="index">&starf;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "Rate",
  props: ["max", "current"],
  computed: {
    getRating: function() {
      return (this.current / this.max) * 100;
    },
  },
};
</script>

<style scoped lang="scss">
.star-rating {
  color: gold;
  display: inline-block;
  font-size: 1.5rem;
  position: relative;
  transform: translate(-6px);
}

.star-rating__max,
.star-rating__current {
  position: absolute;
  top: 0;
}

.star-rating__current {
  overflow: hidden;
  white-space: nowrap;
}
</style>
