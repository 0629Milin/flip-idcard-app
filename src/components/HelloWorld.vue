<template>
   <button @click="openModal">Open Model</button>
  <div class="modal container-fluid" v-if="isOpen">
    <div class="modal-content container-fluid">
      <!-- Your modal content goes here -->
        <ImageCard />
      <div>
        <button class="btn btn-danger btn-sm" style="float: right;" @click="closeModal">Close</button>
      </div>
    </div>
  </div>
</template>

<script>
import ImageCard from './ImageCard.vue';
export default {
  components: {
    ImageCard
  },
  data() {
    return {
      isOpen: false,
    };
  },
  methods: {
    openModal() {
      this.isOpen = true;
    },
    closeModal() {
      this.isOpen = false;
    },
  },
};
</script>

<style scoped>
.modal {
  display: flex;
  align-items: center;
  justify-content: center;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  z-index: 999;
}

.modal-content {
  background-color: white;
  width: 50%;
  padding: 20px;
  border-radius: 5px;
}
</style>