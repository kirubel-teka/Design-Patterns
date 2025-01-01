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

  <app-action></app-action>


    <p>
      

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam rhoncus ante diam, mollis scelerisque eros porta quis. Etiam tempus commodo turpis. Vivamus commodo eros ante, eget laoreet elit interdum sit amet. Fusce rhoncus tellus ultricies sapien tincidunt semper.
 Nunc nec pellentesque lorem. Proin tincidunt arcu sit amet elit molestie, nec rhoncus libero dapibus. Ut lorem diam, volutpat ut consequat non, pharetra ac turpis. Quisque ultrices elit eu vulputate aliquet. Ut ut blandit sem. Maecenas malesuada magna sit amet metus porta, quis sollicitudin turpis tempus. Sed malesuada ante at leo molestie, eu cursus nulla iaculis. Fusce sollicitudin finibus odio, et fringilla augue cursus non.

Aenean efficitur, tortor vel finibus fringilla, libero massa ultricies nisl, vel bibendum purus massa sit amet tortor. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum ut risus ut neque tincidunt interdum. 
Vestibulum ac mauris sed est sollicitudin sodales. 
Nunc blandit est fringilla arcu feugiat finibus eu nec diam. Phasellus dignissim pulvinar lacinia. Nulla sed viverra mi, fermentum laoreet urna. Fusce cursus dui eu sapien aliquet, eu dignissim risus imperdiet. Phasellus sagittis ante eros, eu ultrices risus convallis ac. Vestibulum scelerisque vehicula lacus, at cursus est feugiat ac. Pellentesque enim lectus, tincidunt id mi in, posuere gravida dolor.

Etiam congue leo sed dolor congue ornare.
 Integer tempus nulla risus, in facilisis nisl bibendum vitae. Phasellus vitae tristique velit, nec euismod dui. Proin vulputate tempor nisi, a volutpat tortor egestas ut. Etiam et tincidunt orci, luctus laoreet tellus. Praesent congue interdum porttitor. Morbi nec risus vel risus volutpat gravida. Aenean interdum vitae sapien sed laoreet. Sed sed urna lorem. Etiam venenatis elit non mattis euismod. Aenean accumsan gravida elit, eu interdum elit fringilla sed. Mauris at mollis turpis, sed tristique est.

In nec diam accumsan, vehicula dolor id, sollicitudin diam. 
Proin et lacus urna. Nullam imperdiet, magna in cursus porta, libero lectus lobortis neque, eu tempor enim ex vitae elit. Donec condimentum, dui sit amet ultrices sagittis, urna elit tempus nisi, vitae convallis elit metus ac mauris. Sed tempor elit id risus pharetra, sit amet dignissim diam aliquam. Cras dolor massa, scelerisque id magna eu, ullamcorper efficitur mi. Mauris venenatis sapien sed ante elementum, vitae volutpat nulla ultrices.

Curabitur bibendum viverra efficitur. Maecenas a mattis elit. 
Morbi odio dui, lobortis at egestas id, tincidunt eu nulla. In hac habitasse platea dictumst. Maecenas id velit in nibh varius venenatis ut nec quam. Aliquam erat volutpat. Vivamus ut odio mauris. Phasellus rutrum massa neque, faucibus vestibulum dolor commodo a. Nunc et purus nunc. Phasellus scelerisque eros quis neque varius, egestas tincidunt felis elementum. Nunc orci ligula, feugiat at nibh et, laoreet malesuada eros. Suspendisse et consequat arcu. Praesent et nibh enim. Quisque ut nisi at dolor tristique suscipit dignissim eu neque. 
    </p>
    <p>
      

      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam rhoncus ante diam, mollis scelerisque eros porta quis. Etiam tempus commodo turpis. Vivamus commodo eros ante, eget laoreet elit interdum sit amet. Fusce rhoncus tellus ultricies sapien tincidunt semper.
       Nunc nec pellentesque lorem. Proin tincidunt arcu sit amet elit molestie, nec rhoncus libero dapibus. Ut lorem diam, volutpat ut consequat non, pharetra ac turpis. Quisque ultrices elit eu vulputate aliquet. Ut ut blandit sem. Maecenas malesuada magna sit amet metus porta, quis sollicitudin turpis tempus. Sed malesuada ante at leo molestie, eu cursus nulla iaculis. Fusce sollicitudin finibus odio, et fringilla augue cursus non.
      
      Aenean efficitur, tortor vel finibus fringilla, libero massa ultricies nisl, vel bibendum purus massa sit amet tortor. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum ut risus ut neque tincidunt interdum. 
      Vestibulum ac mauris sed est sollicitudin sodales. 
      Nunc blandit est fringilla arcu feugiat finibus eu nec diam. Phasellus dignissim pulvinar lacinia. Nulla sed viverra mi, fermentum laoreet urna. Fusce cursus dui eu sapien aliquet, eu dignissim risus imperdiet. Phasellus sagittis ante eros, eu ultrices risus convallis ac. Vestibulum scelerisque vehicula lacus, at cursus est feugiat ac. Pellentesque enim lectus, tincidunt id mi in, posuere gravida dolor.
      
      Etiam congue leo sed dolor congue ornare.
       Integer tempus nulla risus, in facilisis nisl bibendum vitae. Phasellus vitae tristique velit, nec euismod dui. Proin vulputate tempor nisi, a volutpat tortor egestas ut. Etiam et tincidunt orci, luctus laoreet tellus. Praesent congue interdum porttitor. Morbi nec risus vel risus volutpat gravida. Aenean interdum vitae sapien sed laoreet. Sed sed urna lorem. Etiam venenatis elit non mattis euismod. Aenean accumsan gravida elit, eu interdum elit fringilla sed. Mauris at mollis turpis, sed tristique est.
      
      In nec diam accumsan, vehicula dolor id, sollicitudin diam. 
      Proin et lacus urna. Nullam imperdiet, magna in cursus porta, libero lectus lobortis neque, eu tempor enim ex vitae elit. Donec condimentum, dui sit amet ultrices sagittis, urna elit tempus nisi, vitae convallis elit metus ac mauris. Sed tempor elit id risus pharetra, sit amet dignissim diam aliquam. Cras dolor massa, scelerisque id magna eu, ullamcorper efficitur mi. Mauris venenatis sapien sed ante elementum, vitae volutpat nulla ultrices.
      
      Curabitur bibendum viverra efficitur. Maecenas a mattis elit. 
      Morbi odio dui, lobortis at egestas id, tincidunt eu nulla. In hac habitasse platea dictumst. Maecenas id velit in nibh varius venenatis ut nec quam. Aliquam erat volutpat. Vivamus ut odio mauris. Phasellus rutrum massa neque, faucibus vestibulum dolor commodo a. Nunc et purus nunc. Phasellus scelerisque eros quis neque varius, egestas tincidunt felis elementum. Nunc orci ligula, feugiat at nibh et, laoreet malesuada eros. Suspendisse et consequat arcu. Praesent et nibh enim. Quisque ut nisi at dolor tristique suscipit dignissim eu neque. 
      </p>

      <p>
      

      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam rhoncus ante diam, mollis scelerisque eros porta quis. Etiam tempus commodo turpis. Vivamus commodo eros ante, eget laoreet elit interdum sit amet. Fusce rhoncus tellus ultricies sapien tincidunt semper.
       Nunc nec pellentesque lorem. Proin tincidunt arcu sit amet elit molestie, nec rhoncus libero dapibus. Ut lorem diam, volutpat ut consequat non, pharetra ac turpis. Quisque ultrices elit eu vulputate aliquet. Ut ut blandit sem. Maecenas malesuada magna sit amet metus porta, quis sollicitudin turpis tempus. Sed malesuada ante at leo molestie, eu cursus nulla iaculis. Fusce sollicitudin finibus odio, et fringilla augue cursus non.
      
      Aenean efficitur, tortor vel finibus fringilla, libero massa ultricies nisl, vel bibendum purus massa sit amet tortor. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum ut risus ut neque tincidunt interdum. 
      Vestibulum ac mauris sed est sollicitudin sodales. 
      Nunc blandit est fringilla arcu feugiat finibus eu nec diam. Phasellus dignissim pulvinar lacinia. Nulla sed viverra mi, fermentum laoreet urna. Fusce cursus dui eu sapien aliquet, eu dignissim risus imperdiet. Phasellus sagittis ante eros, eu ultrices risus convallis ac. Vestibulum scelerisque vehicula lacus, at cursus est feugiat ac. Pellentesque enim lectus, tincidunt id mi in, posuere gravida dolor.
      
      Etiam congue leo sed dolor congue ornare.
       Integer tempus nulla risus, in facilisis nisl bibendum vitae. Phasellus vitae tristique velit, nec euismod dui. Proin vulputate tempor nisi, a volutpat tortor egestas ut. Etiam et tincidunt orci, luctus laoreet tellus. Praesent congue interdum porttitor. Morbi nec risus vel risus volutpat gravida. Aenean interdum vitae sapien sed laoreet. Sed sed urna lorem. Etiam venenatis elit non mattis euismod. Aenean accumsan gravida elit, eu interdum elit fringilla sed. Mauris at mollis turpis, sed tristique est.
      
      In nec diam accumsan, vehicula dolor id, sollicitudin diam. 
      Proin et lacus urna. Nullam imperdiet, magna in cursus porta, libero lectus lobortis neque, eu tempor enim ex vitae elit. Donec condimentum, dui sit amet ultrices sagittis, urna elit tempus nisi, vitae convallis elit metus ac mauris. Sed tempor elit id risus pharetra, sit amet dignissim diam aliquam. Cras dolor massa, scelerisque id magna eu, ullamcorper efficitur mi. Mauris venenatis sapien sed ante elementum, vitae volutpat nulla ultrices.
      
      Curabitur bibendum viverra efficitur. Maecenas a mattis elit. 
      Morbi odio dui, lobortis at egestas id, tincidunt eu nulla. In hac habitasse platea dictumst. Maecenas id velit in nibh varius venenatis ut nec quam. Aliquam erat volutpat. Vivamus ut odio mauris. Phasellus rutrum massa neque, faucibus vestibulum dolor commodo a. Nunc et purus nunc. Phasellus scelerisque eros quis neque varius, egestas tincidunt felis elementum. Nunc orci ligula, feugiat at nibh et, laoreet malesuada eros. Suspendisse et consequat arcu. Praesent et nibh enim. Quisque ut nisi at dolor tristique suscipit dignissim eu neque. 
      </p>

      <p>
      

      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam rhoncus ante diam, mollis scelerisque eros porta quis. Etiam tempus commodo turpis. Vivamus commodo eros ante, eget laoreet elit interdum sit amet. Fusce rhoncus tellus ultricies sapien tincidunt semper.
       Nunc nec pellentesque lorem. Proin tincidunt arcu sit amet elit molestie, nec rhoncus libero dapibus. Ut lorem diam, volutpat ut consequat non, pharetra ac turpis. Quisque ultrices elit eu vulputate aliquet. Ut ut blandit sem. Maecenas malesuada magna sit amet metus porta, quis sollicitudin turpis tempus. Sed malesuada ante at leo molestie, eu cursus nulla iaculis. Fusce sollicitudin finibus odio, et fringilla augue cursus non.
      
      Aenean efficitur, tortor vel finibus fringilla, libero massa ultricies nisl, vel bibendum purus massa sit amet tortor. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Vestibulum ut risus ut neque tincidunt interdum. 
      Vestibulum ac mauris sed est sollicitudin sodales. 
      Nunc blandit est fringilla arcu feugiat finibus eu nec diam. Phasellus dignissim pulvinar lacinia. Nulla sed viverra mi, fermentum laoreet urna. Fusce cursus dui eu sapien aliquet, eu dignissim risus imperdiet. Phasellus sagittis ante eros, eu ultrices risus convallis ac. Vestibulum scelerisque vehicula lacus, at cursus est feugiat ac. Pellentesque enim lectus, tincidunt id mi in, posuere gravida dolor.
      
      Etiam congue leo sed dolor congue ornare.
       Integer tempus nulla risus, in facilisis nisl bibendum vitae. Phasellus vitae tristique velit, nec euismod dui. Proin vulputate tempor nisi, a volutpat tortor egestas ut. Etiam et tincidunt orci, luctus laoreet tellus. Praesent congue interdum porttitor. Morbi nec risus vel risus volutpat gravida. Aenean interdum vitae sapien sed laoreet. Sed sed urna lorem. Etiam venenatis elit non mattis euismod. Aenean accumsan gravida elit, eu interdum elit fringilla sed. Mauris at mollis turpis, sed tristique est.
      
      In nec diam accumsan, vehicula dolor id, sollicitudin diam. 
      Proin et lacus urna. Nullam imperdiet, magna in cursus porta, libero lectus lobortis neque, eu tempor enim ex vitae elit. Donec condimentum, dui sit amet ultrices sagittis, urna elit tempus nisi, vitae convallis elit metus ac mauris. Sed tempor elit id risus pharetra, sit amet dignissim diam aliquam. Cras dolor massa, scelerisque id magna eu, ullamcorper efficitur mi. Mauris venenatis sapien sed ante elementum, vitae volutpat nulla ultrices.
      
      Curabitur bibendum viverra efficitur. Maecenas a mattis elit. 
      Morbi odio dui, lobortis at egestas id, tincidunt eu nulla. In hac habitasse platea dictumst. Maecenas id velit in nibh varius venenatis ut nec quam. Aliquam erat volutpat. Vivamus ut odio mauris. Phasellus rutrum massa neque, faucibus vestibulum dolor commodo a. Nunc et purus nunc. Phasellus scelerisque eros quis neque varius, egestas tincidunt felis elementum. Nunc orci ligula, feugiat at nibh et, laoreet malesuada eros. Suspendisse et consequat arcu. Praesent et nibh enim. Quisque ut nisi at dolor tristique suscipit dignissim eu neque. 
      </p>

    <app-modal :show="open" @hide="open = false"/>
  </div>
</template>

<script>
import EmailInput from '@/components/EmailInput.vue';
import EmojiInput from "@/components/EmojiInput.vue"; 
import AppAction from './components/Action.vue';


export default { 
  name: "App",
  components: {
    EmailInput,
    EmojiInput,
    AppAction,
    
  },
  data() {
    return {
      newsletterName: "",
      newsletterEmail: "",
      emoji: "",
     
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
