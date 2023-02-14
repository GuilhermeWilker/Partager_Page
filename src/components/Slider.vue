<template>
  <div class="slider">
    <img
      src="/images/partager-logo.png"
      alt="logo Partager Player"
      class="logo"
    />

    <div class="box_slider">
      <img
        v-for="(image, index) in images"
        :src="image"
        :key="index"
        :class="{ slide: true, active: currentIndex === index }"
        class="animate__animated animate__pulse"
      />
    </div>
  </div>
</template>

<script>
import "animate.css";

export default {
  name: "Slider",
  data() {
    return {
      currentIndex: 0,
      images: [
        "/images/mobile.png",
        "/images/songmobile.png",
        "/images/aboutmobile.png",
      ],
    };
  },
  computed: {
    activeClass() {
      return (index) => {
        return { slide: true, active: this.currentIndex === index };
      };
    },
  },
  methods: {
    startSlider() {
      setInterval(() => {
        this.currentIndex = (this.currentIndex + 1) % this.images.length;
      }, 3000);
    },
  },
  mounted() {
    this.startSlider();
  },
};
</script>

<style scoped>
.slider {
  content: "";
  border-radius: 20px;
  background-color: #2170e7;
  width: 727px;
  height: 980px;
}

.box_slider {
  overflow: hidden;
}

.slide {
  width: 320px;

  max-width: 600px;
  margin: 10px 30%;
  display: none;
}

.active {
  display: block;

  animation: fadeInLeft;
  animation-duration: 1.5s;
}

.logo {
  padding: 15px;
}

@media (max-width: 1280px) {
  .slider {
    content: "";
    border-radius: 20px;
    background-color: #2170e7;
    width: 680px;
    height: 870px;
  }

  .slide {
    width: 302px;

    margin: 20px 28%;
    display: none;
  }

  .active {
    display: block;

    animation: shakeY;
    animation-duration: 1s;
  }
}

@media (max-width: 1024px) {
  .slider {
    content: "";
    border-radius: 20px;
    background-color: #2170e7;
    width: 680px;
    height: 680px;
  }

  .slide {
    width: 250px;

    margin: 20px 25%;
    display: none;
  }

  .active {
    display: block;

    animation: shakeY;
    animation-duration: 1s;
  }

  .logo {
    padding: 15px;
    width: 95px;
  }
}

@media (max-width: 430px) {
  .slider {
    content: "";
    border-radius: 20px;
    background-color: #2170e7;
    width: 401px;
    height: 560px;
  }

  .slide {
    width: 200px;

    margin: 5px 25%;
    display: none;
  }

  .active {
    display: block;

    animation: shakeY;
    animation-duration: 1s;
  }

  .logo {
    padding: 15px;
    width: 95px;
  }
}
</style>
