<template>
  <div class="desc">
    <p class="desc__text">
      <span class="desc__span">Softline</span>&nbsp;&mdash; ведущий& поставщик
      IT&#8209;решений и&nbsp;сервисов.* Мы&nbsp;предлагаем комплексные
      IT&#8209;решения, облака, программное и&nbsp;аппаратное обеспечение,
      решения по&nbsp;цифровой трансформации и&nbsp;кибербезопасности,
      а&nbsp;также широкий спектр IT&#8209;услуг.
    </p>

    <div class="desc__stat mobile">
      <div class="desc__stat_grid">
        <div class="desc__wrap years">
          <span class="desc__num">> 30 лет</span
          ><span class="desc__span-min">на IT-рынке</span>
        </div>
        <div class="desc__wrap emploees">
          <span class="desc__num">4600</span>
          <span class="desc__span-min">сотрудников в России</span>
        </div>
        <div class="desc__wrap cities">
          <span class="desc__num">25</span
          ><span class="desc__span-min">городов России</span>
        </div>

        <div class="desc__wrap developers">
          <span class="desc__num">2000 +</span
          ><span class="desc__span-min">разработчиков</span>
        </div>
        <div class="desc__wrap students">
          <span class="desc__num">3000 +</span>
          <span class="desc__span-min">
            сотрудников ежегодно проходят оценку и&nbsp;обучение
          </span>
        </div>
      </div>
    </div>

    <div class="desc__stat screen">
      <div class="desc__stat_flex">
        <div class="desc__wrap">
          <span class="desc__num">> 30 лет </span
          ><span class="desc__span-min">на IT-рынке</span>
        </div>
        <div class="desc__wrap">
          <span class="desc__num">4600</span
          ><span class="desc__span-min">сотрудников в России</span>
        </div>
        <div class="desc__wrap">
          <span class="desc__num">25 </span
          ><span class="desc__span-min">городов России</span>
        </div>
      </div>
      <div class="desc__stat_flex">
        <div class="desc__wrap first-num">
          <span class="desc__num">2000 + </span
          ><span class="desc__span-min">разработчиков</span>
        </div>
        <div class="desc__wrap">
          <span class="desc__num">3000 +</span>
          <span class="desc__span-min last-span">
            сотрудников ежегодно проходят оценку и&nbsp;обучение
          </span>
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

.desc {
  width: 100%;
  margin: 97px auto;

  &__text,
  &__span {
    font-family: $condensed;
    font-weight: 600;
    font-size: 32px;
  }

  &__text {
    width: 1110px;
    margin: 0 auto 100px;
    padding: 99px 110px;
    box-shadow: 0px 0px 32px rgba(0, 0, 0, 0.08);
    line-height: 120%;
    text-align: center;
  }
  &__num {
    font-weight: 600;
    font-size: 78px;
    line-height: 83%;
    color: $shiraz-color;
  }

  &__span {
    color: $cardinal-color;

    &-min {
      display: block;
      font-weight: 400;
      font-size: 18px;
      line-height: 27px;
      color: $tundora-color;
    }
  }

  &__stat {
    width: 100%;
    font-weight: 600;
    font-size: 78px;
    line-height: 83%;
    color: $shiraz-color;

    &_flex {
      display: flex;
      justify-content: space-between;
      width: 72%;
      margin: 0 auto;

      &:first-child {
        margin-bottom: 83px;
      }
    }
  }
}
.mobile {
  display: none;
}

.screen {
  display: block;
}
.first-num {
  padding-left: 150px;
}

.last-span {
  width: 55%;
}

@media (width < 1249px) {
  .desc {
    width: 80vw;

    &__content {
      width: 100%;
    }
    &__text {
      width: 100%;
      padding: 64px 50px;
    }
    &__num {
      display: inline-block;
      width: 100%;
      font-size: 40px;
    }

    &__wrap {
      height: 60px;
      margin-bottom: 12px;
    }

    &__text,
    &__span,
    &__span-min {
      font-size: 16px;
    }

    &__span-min {
      display: flex;
      justify-content: center;
      width: 100%;
    }
  }
}

@media (width < 768px) {
  .mobile {
    display: block;
  }

  .screen {
    display: none;
  }
  .desc {
    margin: 75px 0;
    &__text {
      width: 109%;
      margin-bottom: 26px;
      padding: 24px 0px;
      overflow: hidden;
    }
    &__stat {
      width: 100%;

      &_grid {
        display: grid;
        grid-template-columns: 1fr 1fr;
        grid-template-rows: 1fr 1fr 1fr;
        gap: 0px 0px;
        grid-auto-flow: row;
      }
    }
  }
  .cities {
    width: 98px;

    & .desc__num {
      margin-left: 51px;
    }
    & .desc__span-min {
      margin-left: 14px;
    }
  }
  .developers {
    width: 158px;

    & .desc__num {
      margin-left: -21px;
    }

    & .desc__span-min {
      margin-left: -53px;
    }
  }
  .emploees {
    width: 136px;
    & .desc__num {
      margin-left: -9px;
    }

    & .desc__span-min {
      margin-left: -45px;
    }
  }
  .students {
    width: 180px;
    height: 74px;
    margin-left: 50%;

    & .desc__span-min {
      margin-left: -41px;
      text-align: center;
      line-height: 21px;
    }
  }
  .years {
    width: 129px;
  }
}
</style>
