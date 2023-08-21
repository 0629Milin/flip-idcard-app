<template>
  <div>
    <button @click="openModal">Open Modal</button>
    
    <!-- Modal -->
    <div class="modal" :class="{ 'modal-open': isModalOpen }">
      <div class="modal-content">
        <span class="close" @click="closeModal">&times;</span>
        <p>This is a modal popup!</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isModalOpen: false
    };
  },
  methods: {
    openModal() {
      this.isModalOpen = true;
    },
    closeModal() {
      this.isModalOpen = false;
    }
  }
};
</script>

<style>
/* Styles for the modal and button */
.modal {
  display: none; /* Hide modal by default */
  position: fixed;
  z-index: 1;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  overflow: auto;
  background-color: rgba(0,0,0,0.4);
}

.modal-open {
  display: block; /* Show modal when isModalOpen is true */
}

.modal-content {
  background-color: #fff;
  margin: 15% auto;
  padding: 20px;
  border: 1px solid #888;
  width: 80%;
  max-width: 400px;
  position: relative;
}

.close {
  position: absolute;
  top: 0;
  right: 10px;
  font-size: 20px;
  font-weight: bold;
  cursor: pointer;
}
</style>
