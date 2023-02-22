<template>
  <div class="mission bg-mission">
    <h2 class="mission__h2">Миссия Softline</h2>
    <p class="mission__text">
      Мы&nbsp;помогаем организациям трансформироваться, работать эффективно
      и&nbsp;безопасно в&nbsp;условиях цифровой экономики.
    </p>
  </div>
</template>

<script>
export default {
  setup() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/styles.scss";
.bg-mission {
  width: 100%;
  height: 469px;
  margin-bottom: 87px;
  color: #fff;
  background-image: url("../assets/images/bg-mission.svg");
}

.mission {
  padding: 140px 68px;

  &__h2 {
    margin-bottom: 40px;
    text-align: center;
    line-height: 53px;
  }
  &__text {
    width: 97.8%;
    margin: 0 auto;
    font-size: 32px;
    text-align: center;
  }
}

@media (width < 768px) {
  .bg-mission {
    height: 191px;
    background-image: url("../assets/images/bg-mission-min.svg");
    margin-bottom: 33px;
  }
  .mission {
    padding: 32px 1px;

    &__h2 {
      font-size: 28px;
      line-height: 35px;
      margin-bottom: 5px;
    }
    &__text {
      width: 95%;
      font-size: 16px;
      line-height: 21px;
    }
  }
}
</style>
