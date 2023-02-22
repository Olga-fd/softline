<template>
  <div id="regions">
    <div class="back" v-show="showMenu === true"></div>
    <div class="regions__header">
      <div class="container">
        <button
          class="regions__btn"
          :class="{ up: showMenu == true }"
          @click="showMenu = !showMenu"
        >
          Офисы Softline
        </button>
        <nav>
          <ul class="regions__ul">
            <li
              :class="{
                opacity: showMenu === true,
                'active-tab': activeElement == 1,
              }"
              class="regions__li"
              @click="
                {
                  changeRegion();
                  regionsVisible = !regionsVisible;
                  activeElement = 1;
                }
              "
            >
              <span>Все</span>
            </li>
            <li
              :class="{
                opacity: showMenu === true,
                'active-tab': activeElement == 2,
              }"
              class="regions__li"
              @click="
                {
                  changeRegion();
                  moscow = !moscow;
                  activeElement = 2;
                }
              "
            >
              <span>Москва</span>
            </li>
            <li
              :class="{
                opacity: showMenu === true,
                'active-tab': activeElement == 3,
              }"
              class="regions__li"
              @click="
                {
                  changeRegion();
                  center = !center;
                  activeElement = 3;
                }
              "
            >
              <span>Центр</span>
            </li>
            <li
              :class="{
                opacity: showMenu === true,
                'active-tab': activeElement == 4,
              }"
              class="regions__li"
              @click="
                {
                  changeRegion();
                  northWest = !northWest;
                  activeElement = 4;
                }
              "
            >
              <span>Северо&#8209;Запад</span>
            </li>
            <li
              :class="{
                opacity: showMenu === true,
                'active-tab': activeElement == 5,
              }"
              class="regions__li"
              @click="
                {
                  changeRegion();
                  south = !south;
                  activeElement = 5;
                }
              "
            >
              <span>Юг</span>
            </li>
            <li
              :class="{
                opacity: showMenu === true,
                'active-tab': activeElement == 6,
              }"
              class="regions__li"
              @click="
                {
                  changeRegion();
                  volga = !volga;
                  activeElement = 6;
                }
              "
            >
              <span>Волга</span>
            </li>
            <li
              :class="{
                opacity: showMenu === true,
                'active-tab': activeElement == 7,
              }"
              class="regions__li"
              @click="
                {
                  changeRegion();
                  ural = !ural;
                  activeElement = 7;
                }
              "
            >
              <span>Урал</span>
            </li>
            <li
              :class="{
                opacity: showMenu === true,
                'active-tab': activeElement == 8,
              }"
              class="regions__li"
              @click="
                {
                  changeRegion();
                  sibiria = !sibiria;
                  activeElement = 8;
                }
              "
            >
              <span>Сибирь</span>
            </li>
            <li
              :class="{
                opacity: showMenu === true,
                'active-tab': activeElement == 9,
              }"
              class="regions__li"
              @click="
                {
                  changeRegion();
                  east = !east;
                  activeElement = 9;
                }
              "
            >
              <span>Дальний&nbsp;Восток</span>
            </li>
          </ul>
        </nav>
      </div>
    </div>
    <CitiesComponent v-show="showMenu === true" />
    <div id="map">
      <div class="map__cities moscow" v-show="moscow === true"></div>
      <div class="map__cities volga" v-show="volga === true"></div>
      <div class="map__cities center" v-show="center === true"></div>
      <div class="map__cities sibiria" v-show="sibiria === true"></div>
      <div class="map__cities nw" v-show="northWest === true"></div>
      <div class="map__cities east" v-show="east === true"></div>
      <div class="map__cities south" v-show="south === true"></div>
      <div class="map__cities ural" v-show="ural === true"></div>
      <div
        class="map__cities all-cities"
        v-show="regionsVisible === true"
      ></div>
    </div>
  </div>
</template>

<script>
import CitiesComponent from "./CitiesComponent.vue";

export default {
  data() {
    return {
      activeElement: 1,
      showMenu: false,
      regionsVisible: true,
      northWest: false,
      east: false,
      south: false,
      volga: false,
      center: false,
      ural: false,
      moscow: false,
      sibiria: false,
    };
  },
  props: {},
  components: { CitiesComponent },
  methods: {
    changeRegion() {
      this.regionsVisible = false;
      this.moscow = false;
      this.center = false;
      this.northWest = false;
      this.south = false;
      this.volga = false;
      this.ural = false;
      this.sibiria = false;
      this.east = false;
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/styles/styles.scss";

#regions {
  position: relative;

  & nav {
    display: inline-block;
  }
}

#map {
  position: relative;
  width: 100%;
  height: 604px;
  margin-bottom: 100px;
  background-image: url("../assets/images/map/map.png");
  background-position: center;
  background-repeat: no-repeat;
}

.regions {
  &__ul {
    display: flex;
  }

  &__li {
    display: block;
    height: 100%;
    margin-left: 30px;
    padding: 23px 0;
    border-bottom: 3px solid transparent;
    cursor: pointer;

    &:hover {
      color: $shiraz-color;
    }

    & span {
      display: inline-block;
      font: $font;
    }
  }

  &__header {
    width: 100%;
    height: 80px;
    margin-bottom: 90px;
    background: #fff;
    z-index: 1;
    box-shadow: 0px 0px 32px rgba(0, 0, 0, 0.06);
  }

  &__btn {
    z-index: 1;
    width: 226px;
    font-family: $condensed;
    font-size: 24px;
    font-weight: 600;
    line-height: 24px;
    letter-spacing: 0em;
    text-align: left;
    border: none;
    background: transparent;
    background-image: url("../assets/images/down.svg");
    background-repeat: no-repeat;
    background-position: center right 15px;
  }
}
.up {
  background-image: url("../assets/images/up.svg");
}
.map__cities {
  position: absolute;
  background-repeat: no-repeat;
}
.container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 1116px;
  height: 100%;
}

.active-tab {
  color: $shiraz-color;
  border-bottom-color: $shiraz-color;
}

.moscow {
  top: 37.2%;
  left: 12%;
  width: 6%;
  height: 5%;
  background-image: url("../assets/images/map/moscow.svg");
}

.all-cities {
  top: 20.2%;
  left: 2.5%;
  width: 100%;
  height: 80%;
  background-image: url("../assets/images/map/cities.svg");
}

.ural {
  bottom: 35.2%;
  left: 25.2%;
  width: 22%;
  height: 17%;
  background-image: url("../assets/images/map/ural.svg");
}

.south {
  bottom: 30.2%;
  left: 3.7%;
  width: 17%;
  height: 17%;
  background-image: url("../assets/images/map/south.svg");
}

.nw {
  top: 20.8%;
  left: 2.8%;
  width: 27%;
  height: 6%;
  background-image: url("../assets/images/map/nw.svg");
}

.east {
  bottom: 0.5%;
  right: 10.4%;
  width: 13%;
  height: 21%;
  background-image: url("../assets/images/map/east.svg");
}

.sibiria {
  bottom: 10.2%;
  left: 37.8%;
  width: 22%;
  height: 17%;
  background-image: url("../assets/images/map/sib.svg");
}

.center {
  top: 32.8%;
  left: 7.5%;
  width: 14%;
  height: 17%;
  background-image: url("../assets/images/map/center.svg");
}
.volga {
  bottom: 34.8%;
  left: 15.2%;
  width: 12%;
  height: 22%;
  background-image: url("../assets/images/map/volga.svg");
}

.back {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 1;
  background-color: #f5f5f5;
  opacity: 0.7;
  transition: height 2s ease;
}

.opacity {
  opacity: 0.1;
}

@media (width < 1249px) {
  .container {
    flex-direction: column;
    width: 100%;
    align-items: flex-start;
  }

  .regions {
    // padding: 0 3px;
    // margin-bottom: 50px;
    // overflow-x: scroll;
    // touch-action: pan-y, pan-x;
    // -ms-overflow-style: none;
    // scrollbar-width: none;

    // &::-webkit-scrollbar {
    //   display: none;
    // }
    &__btn {
      padding-left: 0;
      font-size: 20px;
    }
    &__ul {
      padding-left: 0;
    }
    &__li {
      &:first-child {
        margin-left: 0;
      }

      & li {
        font-size: 14px;
      }
    }
  }
}

@media (width < 768px) {
  #regions {
    padding: 0 3px;
    margin-bottom: 50px;
    overflow-x: scroll;
    touch-action: pan-y, pan-x;
    -ms-overflow-style: none;
    scrollbar-width: none;

    &::-webkit-scrollbar {
      display: none;
    }
  }

  .regions {
    &__header {
      width: 100%;
      height: 100px;
      padding-top: 18px;
    }
    &__btn {
      font-size: 20px;
      background-position: center right 75px;
    }
    &__li {
      margin-left: 18px;
      padding: 15px 0;

      & span {
        font-size: 14px;
      }
    }
  }

  .container {
    padding-left: 5px;
  }

  #map {
    width: 1250px;
    margin: -157px 0 -163px -169px;
    transform: scale(0.749);
  }

  .back {
    height: 80%;
  }
}
</style>
