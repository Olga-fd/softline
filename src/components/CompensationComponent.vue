<template>
  <div class="compensation-block">
    <h2 class="compensation-block__header">Компенсационный пакет</h2>
    <div class="compensation-block__row">
      <div class="compensation-block__wrap">
        <div class="compensation-block__icon icon1"></div>
        <span class="compensation-block__span">ДМС</span>
      </div>

      <div class="compensation-block__wrap">
        <div class="compensation-block__icon icon2"></div>
        <span class="compensation-block__span span2"
          >Выходной в&nbsp;день&nbsp;рождения</span
        >
      </div>

      <div class="compensation-block__wrap">
        <div class="compensation-block__icon icon3"></div>
        <span class="compensation-block__span"
          >Корпоративная мобильная&nbsp;связь
        </span>
      </div>

      <div class="compensation-block__wrap">
        <div class="compensation-block__icon icon4"></div>
        <span class="compensation-block__span discount"
          >Корпоративные скидки на&nbsp;спорт</span
        >
      </div>

      <div class="compensation-block__wrap">
        <div class="compensation-block__icon icon5"></div>
        <span class="compensation-block__span">LTI</span>
      </div>
    </div>

    <div class="compensation-block__row2 row2">
      <div class="compensation-block__text">
        <p class="compensation-block__text1">
          Программа дополнительной мотивации
        </p>
        <p class="compensation-block__text2">доплата 12% от суммы</p>
      </div>
      <div class="compensation-block__sub">
        <div class="compensation-block__wrap">
          <div class="compensation-block__icon icon6"></div>
          <span class="compensation-block__span">Оргтехники</span>
        </div>

        <div class="compensation-block__wrap">
          <div class="compensation-block__icon icon1"></div>
          <span class="compensation-block__span">ДМС</span>
        </div>

        <div class="compensation-block__wrap">
          <div class="compensation-block__icon icon7"></div>
          <span class="compensation-block__span">Ипотеки</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@import "../assets/styles/styles.scss";

.compensation-block {
  width: 1110px;
  height: 856px;
  margin: 0 auto 100px;
  padding: 62px 76px;
  box-shadow: 0px 0px 32px rgba(0, 0, 0, 0.08);
  box-sizing: border-box;

  &__header {
    margin-bottom: 32px;
  }

  &__row {
    display: flex;
    justify-content: space-between;
  }

  &__wrap {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 178px;
  }

  &__icon {
    width: 110px;
    height: 110px;
    margin-bottom: 10px;
    background-color: rgba(0, 0, 0, 0.05);
    background-repeat: no-repeat;
    background-position: center;
    border-radius: 50px;
  }

  &__span {
    text-align: center;
  }

  &__row2 {
    margin-top: 58px;
    padding-top: 70px;
  }

  &__sub {
    display: flex;
    justify-content: center;
    flex-direction: row;
  }

  &__text {
    margin-bottom: 50px;
    font-size: 40px;
    font-weight: 600;
    line-height: 48px;
    letter-spacing: 0em;
    text-align: center;

    &2 {
      color: $cardinal-color;
    }
  }
}

.icon1 {
  background-image: url("../assets/images/icons/dms.svg");
}
.icon2 {
  background-image: url("../assets/images/icons/holiday.svg");
}
.icon3 {
  background-image: url("../assets/images/icons/mobile.svg");
}
.icon4 {
  background-image: url("../assets/images/icons/gym.svg");
}
.icon5 {
  background-image: url("../assets/images/icons/hands.svg");
}
.icon6 {
  background-image: url("../assets/images/icons/print.svg");
}
.icon7 {
  background-image: url("../assets/images/icons/house.svg");
}

.span2 {
  display: inline-block;
  padding: 0 10px;
}

.row2 {
  padding: 0 30px;
  border-top: 1px solid rgba(0, 0, 0, 0.1);
  padding-top: 70px;
}

@media (width < 1249px) {
  .compensation-block {
    height: auto;
  }
}

@media (width < 768px) {
  .compensation-block {
    width: 100%;
    margin-bottom: 50px;
    padding: 24px 0 0;

    &__header {
      margin-bottom: 33px;
    }

    &__row,
    &__sub {
      flex-wrap: wrap;
      justify-content: space-around;
    }

    &__row2 {
      margin-top: 0;
    }

    &__text {
      font-size: 22px;
      margin-bottom: 30px;

      &1,
      &2 {
        line-height: 26.4px;
      }
    }

    &__icon {
      width: 80px;
      height: 80px;
      margin-bottom: 10px;
      background-color: rgba(0, 0, 0, 0.05);
      background-repeat: no-repeat;
      background-position: center;
      background-size: 50%;
      border-radius: 50px;
    }

    &__span {
      font-size: 16px;
      line-height: 17.6px;
    }

    &__wrap {
      width: 101px;
      margin-bottom: 25px;
    }
  }

  .row2 {
    padding: 24px 0 0;
  }
}
</style>
