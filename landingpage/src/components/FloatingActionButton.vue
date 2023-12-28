<script>
import UpToTopIcon from './icons/UpToTopIcon.vue';

export default {
  name: 'FloatingActionButton',
  components: {
    UpToTopIcon
  }
};
</script>

<template>
  <div class="fab-container">
    <button @click="$emit('scroll-to-top')" type="button" class="btn btn-info rounded-circle fab">
      <div class="fab-icon-container">
        <UpToTopIcon />
      </div>
    </button>
  </div>
</template>

<style scoped>

.fab-container {
  position: fixed;
  bottom: 30px;
  right: 30px;
}

.fab {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  background-color: #041421;
  color: #fff;
  box-shadow: 0px 2px 5px 0px rgba(0, 0, 0, 1);
  border: none;
  outline: none;
}

.fab-icon-container {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100%;
}
</style>
