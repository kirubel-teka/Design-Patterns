<template>
  <div class="modal" :style="{ display: show ? 'block' : 'none' }">
    <div class="modal-dialog" style="z-index: 5000">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title">Awesome Title</h5>
          <button type="button" class="close" style="margin-left: 68%;" @click="close">
            <span>x</span>
          </button>
        </div>
        <div class="modal-body">
          <p>Awesome content.</p>
        </div>
      </div>
    </div>
    <div class="modal-backdrop show"></div>
  </div>
</template>

<script>
export default {
  name: "AppModal",
  props: ["show"],
  methods: {
    close() {
      this.$emit("hide");
    },
    handler(e) {
      if (e.code === 'Escape' && this.show) {
        this.close();
      }
    },

    handleOutsideClick(event) {
      // Find the modal-content element
      const modalContent = this.$el.querySelector('.modal-content');
      // Check if the click was outside modal-content and modal is visible
      if (this.show && modalContent && !modalContent.contains(event.target)) {
        this.close();
        console.log('closed it')
      }
    },
  },
  created() {
    document.addEventListener('keydown', this.handler);
  },

  mounted() {
      console.log('Component mounted, attaching listeners');
      document.addEventListener('click', this.handleOutsideClick, { capture: true });
      document.addEventListener('keydown', this.handleEscape);
   
  },

  unmounted() {
    document.removeEventListener('click', this.handleOutsideClick, { capture: true });
    document.removeEventListener('keydown', this.handler);
  }
};
</script> 





 
