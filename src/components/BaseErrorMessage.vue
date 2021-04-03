<template>
  <div class="error">
    <h5 class="error-title">{{ data.title }}</h5>
    <p class="error-message">{{ data.message }}</p>
  </div>
</template>

<script>
export default {
  props: ["data"],
};
</script>

<style scoped>
.error {
  display: flex;
  flex-direction: column;
  justify-content: center;
  background-color: rgb(208, 84, 84);
}
.error-title {
  font-weight: bold;
  color: #fff;
  font-style: italic;
  font-size: 20px;
}
.error-message {
  font-size: 16px;
  font-weight: 100;
}
</style>
