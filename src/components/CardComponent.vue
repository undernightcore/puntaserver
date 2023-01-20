<template>
  <div class="card">
    <h3>{{ title }}</h3>
    <p>{{ description }}</p>
  </div>
</template>

<script lang="ts">
export default { name: "CardComponent" };
</script>
<script setup lang="ts">
defineProps({
  title: {
    default: "",
  },
  description: {
    default: "",
  },
});
</script>

<style lang="scss" scoped>
.card {
  cursor: pointer;
  justify-content: flex-end;
  & > h3 {
    margin: 0;
  }
  display: flex;
  flex-direction: column;
  border: 2px var(--color-accent) solid;
  border-radius: 20px;
  height: 300px;
  width: 300px;
  padding: 20px;
  box-sizing: border-box;
}
</style>
