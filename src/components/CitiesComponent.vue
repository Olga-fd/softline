<template>
  <div class="wrapper">
    <div class="wrapper__ul">
      <div class="wrapper__li header-table">
        <span class="bold">Москва</span>
        <span class="arrow"></span>
      </div>
    </div>

    <div class="wrapper__ul">
      <div class="wrapper__li header-table" @click="regCenter = !regCenter">
        <span class="bold" :class="{ 'active-region': regCenter == true }"
          >Центр</span
        >
        <span class="arrow" :class="{ reverse: regCenter == true }"></span>
      </div>
      <div class="wrapper__li" :class="{ 'js-center': regCenter == false }">
        <span class="wrapper__li">Воронеж</span>
        <span class="wrapper__li">Ярославль</span>
        <span class="wrapper__li">Белгород</span>
      </div>
    </div>

    <div class="wrapper__ul">
      <div class="wrapper__li header-table" @click="regNorth = !regNorth">
        <span class="bold" :class="{ 'active-region': regNorth == true }"
          >Северо&#8209;Запад</span
        >
        <span class="arrow" :class="{ reverse: regNorth == true }"></span>
      </div>
      <div class="wrapper__li" :class="{ 'js-north': regNorth == false }">
        <span class="wrapper__li">Санкт&#8209;Петербург</span>
        <span class="wrapper__li">Калининград</span>
      </div>
    </div>

    <div class="wrapper__ul">
      <div class="wrapper__li header-table" @click="regSouth = !regSouth">
        <span class="bold" :class="{ 'active-region': regSouth == true }"
          >Юг</span
        >
        <span class="arrow" :class="{ reverse: regSouth == true }"></span>
      </div>
      <div class="wrapper__li" :class="{ 'js-south': regSouth == false }">
        <span class="wrapper__li">Ростов&#8209;на&#8209;Дону</span>
        <span class="wrapper__li">Краснодар</span>
        <span class="wrapper__li">Волгоград</span>
      </div>
    </div>

    <div class="wrapper__ul">
      <div class="wrapper__li header-table" @click="regVolga = !regVolga">
        <span class="bold" :class="{ 'active-region': regVolga == true }"
          >Волга</span
        >
        <span class="arrow" :class="{ reverse: regVolga == true }"></span>
      </div>
      <div class="wrapper__li" :class="{ 'js-volga': regVolga == false }">
        <span class="wrapper__li">Казань</span>
        <span class="wrapper__li">Самара</span>
        <span class="wrapper__li">Уфа</span>
        <span class="wrapper__li">Оренбург</span>
        <span class="wrapper__li">Нижний&nbsp;Новгород</span>
      </div>
    </div>

    <div class="wrapper__ul">
      <div class="wrapper__li header-table" @click="regUral = !regUral">
        <span class="bold" :class="{ 'active-region': regUral == true }"
          >Урал</span
        >
        <span class="arrow" :class="{ reverse: regUral == true }"></span>
      </div>
      <div class="wrapper__li" :class="{ 'js-ural': regUral == false }">
        <span class="wrapper__li">Екатеринбург</span>
        <span class="wrapper__li">Челябинск</span>
        <span class="wrapper__li">Пермь</span>
        <span class="wrapper__li">Сургут</span>
        <span class="wrapper__li">Тюмень</span>
        <span class="wrapper__li">Ижевск</span>
      </div>
    </div>

    <div class="wrapper__ul">
      <div class="wrapper__li header-table" @click="regSib = !regSib">
        <span class="bold" :class="{ 'active-region': regSib == true }"
          >Сибирь</span
        >
        <span class="arrow" :class="{ reverse: regSib == true }"></span>
      </div>
      <div class="wrapper__li" :class="{ 'js-sib': regSib == false }">
        <span class="wrapper__li">Новосибирск</span>
        <span class="wrapper__li">Омск</span>
        <span class="wrapper__li">Томск</span>
        <span class="wrapper__li">Красноярск</span>
        <span class="wrapper__li">Иркутск</span>
      </div>
    </div>

    <div class="wrapper__ul">
      <div class="wrapper__li header-table" @click="regEast = !regEast">
        <span class="bold" :class="{ 'active-region': regEast == true }"
          >Дальний&nbsp;Восток</span
        >
        <span class="arrow" :class="{ reverse: regEast == true }"></span>
      </div>
      <div class="wrapper__li" :class="{ 'js-east': regEast == false }">
        <span class="wrapper__li">Хабаровск</span>
        <span class="wrapper__li">Владивосток</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      regCenter: false,
      regUral: false,
      regVolga: false,
      regSouth: false,
      regNorth: false,
      regEast: false,
      regSib: false,
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/styles.scss";

.arrow {
  display: none;
}
.wrapper {
  position: absolute;
  top: 13%;
  left: 0;
  z-index: 1;
  display: flex;
  max-width: 1250px;
  height: 272px;
  padding: 26px 69px;
  background-color: #fff;
  box-shadow: 0px 0px 32px rgba(0, 0, 0, 0.06);
  box-sizing: border-box;
  transition: all 3s ease;

  &__ul {
    display: block;
    margin-right: 24px;
    padding: 0;
  }
  &__li {
    display: block;
    font-family: $nova;
    font-size: 18px;
    line-height: 31px;
    letter-spacing: 0em;
  }
}

.header-table {
  display: flex;
  align-items: center;
}

.bold {
  font-size: 21px;
  font-weight: 600;
}

@media (width < 768px) {
  .active-region {
    color: $shiraz-color;
  }
  .js {
    &-sib,
    &-center,
    &-volga,
    &-south,
    &-east,
    &-north,
    &-ural {
      display: none;
    }
  }
  .wrapper {
    width: 100% !important;
    height: auto;
    flex-wrap: wrap !important;
    top: 7%;
    left: 0;
    padding: 5px;
    box-shadow: none;

    &__ul {
      margin-bottom: 15px;
    }

    &__li {
      font-size: 14px;
      line-height: 21.5px;
    }
  }

  .bold {
    font-size: 15px;
    line-height: 27px;
    cursor: pointer;
  }

  .arrow {
    display: inline-block;
    width: 13px;
    height: 10px;
    margin-left: 4px;
    transform: scale(1.3);
    background-image: url("../assets/images/list-arrow-down.svg");
    background-position-y: center;
    background-repeat: no-repeat;
  }

  .reverse {
    margin-left: 0;
    transform: scale(1.3) rotate(0.5turn);
  }
}
</style>
