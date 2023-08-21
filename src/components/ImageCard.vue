<template>
  <div class="image-container">
    <div class="image-card" :class="{ 'flipped': isFlipped }">
      <div class="front">
        <img :src="frontImageUrl" alt="Front Image" />
      </div>
      <div class="back">
        <img :src="backImageUrl" alt="Back Image" />
      </div>
    </div>
    <div>
        <a @click="flipImage">Click to Flip</a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isFlipped: false,
      frontImageUrl: 'https://picsum.photos/id/237/200/300',
      backImageUrl: 'https://picsum.photos/seed/picsum/200/300'
    };
  },
  methods: {
    flipImage() {
      this.isFlipped = !this.isFlipped;
    },
  }
};
</script>

<style scoped>

.image-container {
  position: relative;
  width: 200px;
  height: 300px;
}

.image-card {
  width: 100%;
  height: 100%;
  transform-style: preserve-3d;
  transition: transform 0.5s ease;
}

.front,
.back {
  position: absolute;
  width: 100%;
  height: 100%;
  backface-visibility: hidden;
}

.front {
  display: flex;
  justify-content: center;
  align-items: center;
}

.back {
  transform: rotateY(180deg);
  display: flex;
  justify-content: center;
  align-items: center;
}

img {
  width: 100%;
  height: 100%;
}

.flipped {
  transform: rotateY(180deg);
}

</style>
