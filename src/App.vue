<template>
  <div id="app" class="row d-flex justify-content-center">
    <div class="col-md-6 mt-3">
      <div class="card">
        <div class="card-header">Newsletter</div>
        <div class="card-body">
          <form @submit.prevent="submit">
            <div class="mb-2">
              <input
                type="text"
                class="form-control"
                placeholder="Name"
                :value="newsletterName"
                @input="newsletterName = $event.target.value"
              />
            </div>
            <div class="mb-2">
              <email-input v-model:email="newsletterEmail"></email-input>
              
            
              <!-- <email-input :modelValue="newsletterEmail"
              @update:modelValue="newsletterEmail = $event">

              </email-input> -->
            </div>
            <div class="mb-2">
              <EmojiInput v-model="emoji" :options="{ position: 'bottom' }" />
            </div>
            
            <button type="submit" class="btn btn-primary">Submit</button>
          </form>
          
        </div>
      </div>
    </div>

    <div class="mt-2 ml-2">
      <button type="button" class="btn btn-primary" @click="open = true">
        Open
      </button>
    </div>

    <app-modal :show="open" @hide="open = false" />
  </div>
</template>

<script>
import EmailInput from '@/components/EmailInput.vue';
import EmojiInput from "@/components/EmojiInput.vue";
import AppModal from "@/components/Modal.vue";


export default { 
  name: "App",
  components: {
    EmailInput,
    EmojiInput,
    AppModal,
  },
  data() {
    return {
      newsletterName: "",
      newsletterEmail: "",
      emoji: "",
      open: false,
    };
  },
  methods: {
    submit() {
      console.log("Newletter Submitted", {
        name: this.newsletterName,
        email: this.newsletterEmail,
      });
      console.log("Emoji: ", this.emoji);
    },
  },
};
</script>

<style src="bootstrap/dist/css/bootstrap.css"></style>
