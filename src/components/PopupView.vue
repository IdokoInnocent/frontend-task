<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="modal">
    <slot />
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.modal {
  position: absolute;
  top: 60%;
  left: 50%;
  transform: translate(-50%, -50%);
  background: #15141b;
  width: 30%;
  height: 47.5rem;
  padding: 6rem;
  border-radius: 2rem;
  box-shadow: 0 3rem 5rem rgba(0, 0, 0, 0.3);
  z-index: 10;
}

.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 200rem;
  background-color: rgba(0, 0, 0, 0.6);
  backdrop-filter: blur(2px);
  z-index: 5;
}

// Popup
.popup-icon {
  position: relative;
  top: 4rem;

  &__ellipse{
    position: relative;
    left: 2rem;
  }
  &__verified{
    position: relative;
    bottom: 4rem;
    left: -5.5rem;
  }
}

.popup-text {
  position: relative;
  top: 7rem;
  text-align: center;
  h4{
    color: var(--primary-text);
    font-size: 2.4rem;
  }
  p {
   color: rgba(255, 255, 255, 0.9);
   font-size: 1.6rem;
  }
}

// .close-modal {
//   position: absolute;
//   top: 1.2rem;
//   right: 2rem;
//   font-size: 5rem;
//   color: #333;
//   cursor: pointer;
//   border: none;
//   background: none;
// }
</style>
