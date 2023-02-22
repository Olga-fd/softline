<template>
  <header class="header fixed-box">
    <IconLogo />
    <nav>
      <ul class="header__ul">
        <li><a href="#">Облачные решения</a></li>
        <li><a href="#">Кибербезопасность</a></li>
        <li><a href="#">Импортозамещение</a></li>
        <li><a href="#">Цифровая трансформация</a></li>
      </ul>
    </nav>
  </header>
</template>

<script>
import IconLogo from "./icons/IconLogo.vue";

export default {
  components: {
    IconLogo,
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/styles.scss";

.header {
  height: 85px;
  justify-content: space-between;
  align-items: center;

  &,
  &__ul {
    display: flex;
  }

  &__ul li {
    font-family: $condensed;
    font-size: 19px;
    font-weight: 400;
    color: $tundora-color;

    &:not(:last-child) {
      padding-right: 20px;
    }
  }
}
.fixed-box {
  width: 1107px;
  margin: 0 auto;
}

@media (width < 768px) {
  .header {
    flex-wrap: wrap;
    align-items: start;
    height: 110px;
    padding: 16px 5px;
    &__ul {
      flex-wrap: wrap;
      padding-inline-start: 0;

      & li {
        font-size: 14px;
        margin-bottom: -7px;
      }
    }
  }

  .fixed-box {
    width: 100%;
  }
}
</style>
