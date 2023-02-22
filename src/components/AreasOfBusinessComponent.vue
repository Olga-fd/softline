<template>
  <div>
    <h2>Направления бизнеса</h2>
    <div class="grid">
      <div class="grid__content grid-bg1">
        <div class="grid__wrap">
          <h3 class="grid__header">Решения Softline</h3>
          <p class="grid__text">
            ГК&nbsp;Softline предлагает клиентам собственную линейку
            оборудования (ПК, серверы, торговое оборудование и&nbsp;проч.),
            разработку программных продуктов, облачных решений, решений
            в&nbsp;области информационной безопасности.
          </p>
        </div>
      </div>
      <div class="grid__content grid-bg2">
        <div class="grid__wrap">
          <h3 class="grid__header">Кибербезопасность</h3>
          <p class="grid__text">
            Softline обладает всеми необходимыми государственными лицензиями для
            организации проектов по&nbsp;информационной безопасности
            и&nbsp;аттестации.
          </p>
        </div>
      </div>
      <div class="grid__content grid-bg3">
        <div class="grid__wrap">
          <h3 class="grid__header">Импортозамещение</h3>
          <p class="grid__text">
            ГК&nbsp;Softline обладает широчайшим портфелем решений и&nbsp;услуг
            для импортозамещения, включая&nbsp;ПО и&nbsp;оборудование
            собственного производства.
          </p>
        </div>
      </div>
      <div class="grid__content grid-bg4">
        <div class="grid__wrap">
          <h3 class="grid__header">Облачные решения</h3>
          <p class="grid__text">
            Softline использует современные облачные решения как российских, так
            и&nbsp;международных вендоров для масштабирования бизнеса своих
            клиентов. Подписки, услуги, трансформация.
          </p>
        </div>
      </div>
      <div class="grid__content grid-bg5">
        <div class="grid__wrap">
          <h3 class="grid__header">Цифровая трансформация и разработка ПО</h3>
          <p class="grid__text">
            Softline использует современные технологи и&nbsp;новые возможности
            для увеличения производительности бизнеса заказчика. В&nbsp;штате
            ГК&nbsp;Softline&nbsp;&mdash; 2000+&nbsp;разработчиков, которые
            трансформируют&nbsp;ПО под нужды конкретного предприятия.
          </p>
        </div>
      </div>
      <div class="grid__content grid-bg6">
        <div class="grid__wrap">
          <h3 class="grid__header">Техническая поддержка Softline</h3>
          <p class="grid__text">
            200+&nbsp;инженеров, 24&nbsp;часа в&nbsp;сутки, 7&nbsp;дней
            в&nbsp;неделю, 12&nbsp;месяцев в&nbsp;году, сервисное партнерство
            с&nbsp;30+&nbsp;мировыми производителями.
          </p>
        </div>
      </div>
    </div>
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

h2 {
  margin-bottom: 41px;
}
.grid {
  display: grid;
  grid-template-columns: repeat(2, 50%);
  grid-template-rows: repeat(6, 1ft);
  column-gap: 9px;
  row-gap: 20px;
  margin-bottom: 100px;

  &__content {
    position: relative;
    width: 615px;
    height: 260px;
  }

  &-bg {
    &1,
    &2,
    &3,
    &4,
    &5,
    &6 {
      background-repeat: no-repeat;
    }
    &1 {
      background-image: url("../assets/images/areas/area2.jpg");
    }
    &2 {
      background-image: url("../assets/images/areas/area1.jpg");
    }
    &3 {
      background-image: url("../assets/images/areas/area3.jpg");
    }
    &4 {
      background-image: url("../assets/images/areas/area4.jpg");
    }
    &5 {
      background-image: url("../assets/images/areas/area5.jpg");
    }
    &6 {
      background-image: url("../assets/images/areas/area6.jpg");
    }
  }

  &__wrap {
    box-sizing: border-box;
    position: absolute;
    bottom: 0;
    display: flex;
    align-items: flex-start;
    flex-direction: column;

    width: 100%;
    height: 80px;
    padding: 28px 20px;
    color: #fff;
    background-color: $pickled-bluewood-color;
  }

  &__wrap:hover {
    height: 100%;
    transition: height 0.2s ease-in-out;

    & .grid__text {
      display: block;
      width: 480px;
    }

    & .grid__header {
      margin-bottom: 20px;
    }
  }

  &__header {
    font-weight: 600;
    font-size: 24px;
    line-height: 100%;
  }

  &__text {
    display: none;
    font-size: 17px;
  }
}

@media (width < 1250px) {
  .grid__content {
    width: 100%;
  }
}

@media (width < 768px) {
  h2 {
    margin-bottom: 7px;
  }
  .grid {
    display: flex;
    margin-bottom: 31px;
    flex-direction: column;
    row-gap: 12px;

    &__content {
      width: 100%;
      height: 60px;

      &:hover {
        height: 240px;
        transition: height 0.5s ease-in-out;
      }
    }

    &__header {
      width: 85%;
    }

    &__wrap {
      justify-content: center;
      height: 100%;
      padding: 0;
      padding-left: 10px;
      background-image: url("../assets/images/white-arrow.svg");
      background-repeat: no-repeat;
      background-position: center right 15px;

      &:hover {
        padding: 20px 10px;
        justify-content: flex-start;
        background-image: url("../assets/images/white-arrow-up.svg");
        background-position: top 20px right 15px;

        & .grid__text {
          width: 100%;
        }

        & .grid__header {
          margin-bottom: 10px;
        }
      }
    }

    &__header {
      font-size: 20px;
    }

    &__text {
      font-size: 16px;
      line-height: 23px;
    }
  }
}
</style>
