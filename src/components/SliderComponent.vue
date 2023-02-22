<template>
  <div class="slider__content">
    <div class="container">
      <h2 class="slider__content_header">Корпоративная жизнь</h2>
      <button class="prev" @click="slide(-1)"></button>
      <button class="next" @click="slide(1)"></button>

      <div class="slider__content_images" @click="slide(1)">
        <img
          class="slider__content_img"
          src="../assets/images/slides/slide1.webp"
          alt=""
          v-show="indexValue == 1"
        />
        <img
          class="slider__content_img"
          src="../assets/images/slides/slide2.webp"
          alt=""
          v-show="indexValue == 2"
        />
        <img
          class="slider__content_img"
          src="../assets/images/slides/slide3.webp"
          alt=""
          v-show="indexValue == 3"
        />
        <img
          class="slider__content_img"
          src="../assets/images/slides/slide4.webp"
          alt=""
          v-show="indexValue == 4"
        />
        <img
          class="slider__content_img"
          src="../assets/images/slides/slide5.webp"
          alt=""
          v-show="indexValue == 5"
        />
      </div>

      <div class="btn-sliders">
        <span class="btn-sliders__span active" @click="changeSlide(1)"></span>
        <span class="btn-sliders__span" @click="changeSlide(2)"></span>
        <span class="btn-sliders__span" @click="changeSlide(3)"></span>
        <span class="btn-sliders__span" @click="changeSlide(4)"></span>
        <span class="btn-sliders__span" @click="changeSlide(5)"></span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      indexValue: 1,
    };
  },
  setup() {
    return {};
  },
  methods: {
    changeSlide(page = 1) {
      let active = document.querySelector(".active");
      let target = event.target;
      this.indexValue = page;
      this.changeColor(active, target);
    },
    changeColor(active, target) {
      if (active !== null) {
        active.classList.remove("active");
        target.classList.add("active");
      } else {
        target.classList.add("active");
      }
    },
    slide(pageNum) {
      if (pageNum == -1 && this.indexValue == 1) {
        this.indexValue = 5;
      } else if (pageNum == 1 && this.indexValue == 5) {
        this.indexValue = 1;
      } else if (this.indexValue > 0 || this.indexValue < 0) {
        this.indexValue += pageNum;
      }
      let active = document.querySelector(".active");
      let target =
        document.querySelectorAll(".btn-sliders__span")[this.indexValue - 1];
      this.changeColor(active, target);
    },
  },
};
</script>

<style lang="scss" scoped>
h2 {
  text-align-last: left;
  line-height: 1;
}
.slider__content {
  width: 100%;
  margin-bottom: 100px;
  overflow: hidden;

  &_images {
    height: 834px;
    margin: 0 auto;
    margin-bottom: 23px;
  }
  &_img {
    height: 100%;
    width: 100%;
    animation: 1s alternate slidein;
  }
}

@keyframes slidein {
  from {
    opacity: 30%;
  }

  to {
    opacity: 100%;
  }
}

.container {
  position: relative;
}

.btn-sliders {
  width: 100%;

  &__span {
    display: inline-block;
    width: 216px;
    height: 6px;
    margin: 0 3px;
    background: rgba($color: #000000, $alpha: 0.1);
    cursor: pointer;
  }
}

button {
  position: absolute;
  top: 10px;
  right: 0;
  width: 56px;
  height: 56px;
  background: #f0f0f0;
  background-repeat: no-repeat;
  background-position: center;
  border: none;
  border-radius: 64.2857px;
}

.active {
  background: #a30c33;
}

.prev {
  background-image: url(../assets/images/prev.svg);
  transform: translateX(-72px);
}

.next {
  background-image: url(../assets/images/prev.svg);
  transform: rotate(0.5turn);
}

@media (width < 768px) {
  .slider__content {
    margin-bottom: 0;
    &_images {
      height: 65%;
    }

    &_img {
      object-fit: contain;
    }

    &_header {
      margin-bottom: 15px;
    }
  }

  .container {
    width: 100%;
  }

  .next,
  .prev,
  .btn-sliders {
    display: none;
  }
}
</style>
