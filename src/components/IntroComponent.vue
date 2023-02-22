<template>
  <div class="intro-bg">
    <div class="intro-bg__content">
      <h1>Softline</h1>
      <p class="intro-bg__text">
        Поставщик услуг цифровой трансформации и&nbsp;кибербезопасности
      </p>
      <ButtonComponent />
    </div>
  </div>
</template>

<script>
import ButtonComponent from "./UI/ButtonComponent.vue";
export default {
  components: { ButtonComponent },
};
</script>
<style lang="scss">
h1 {
  display: none;
}
.intro-bg {
  position: relative;
  width: 100%;
  height: 600px;
  background-image: url("../assets/images/bg.webp");
  background-repeat: no-repeat;

  &__content {
    position: absolute;
    top: 26%;
    left: 70px;
  }

  &__text {
    max-width: 718px;
    margin-bottom: 59px;
    font-weight: 500;
    font-size: 58px;
    line-height: 56px;
  }
}

@media (width < 1249px) {
  .intro-bg {
    &__content {
      top: 15%;
      left: 5px;
    }

    &__text {
      width: 80%;
      font-size: 3rem;
      line-height: 100%;
    }
  }
}

@media (width < 768px) {
  .intro-bg {
    background-size: cover;

    &__text {
      width: 43%;
      font-size: 1.8rem;
      line-height: 100%;
      margin-bottom: 20px;
    }
  }
}

@media (width < 370px) {
  .intro-bg {
    height: 300px;
    background-size: auto;
    background-image: url("../assets/images/bg-min.webp");
    &__text {
      width: 67%;
    }
  }
}
</style>
