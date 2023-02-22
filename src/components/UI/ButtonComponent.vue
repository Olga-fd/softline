<template>
  <a href="https://softline.ru" class="btn" target="_blank">Наш сайт</a>
</template>

<script>
export default {
  name: "ButtonComponent",
};
</script>

<style lang="scss">
@import "../../assets/styles/styles.scss";
.btn {
  padding: 15px 25px;
  margin-bottom: 20px;
  font-family: $condensed;
  font-weight: 600;
  color: #fff;
  background-color: $cardinal-color;
  border-radius: 8px;
  border: none;
}
.btn:hover {
  background-color: $brick-red-color;
}

@media (width < 1249px) {
  .btn {
    padding: 3.5px 27.5px;
    font-size: 16px;
  }
}
</style>
