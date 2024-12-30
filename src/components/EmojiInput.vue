<template>
  <div class="input-group">
    <input
      type="text"
      class="form-control"
      :value="modelValue"
      @input="updateInput"
    />
    <div class="input-group-append">
      <button class="btn btn-outline-secondary" type="button" ref="emojiBtn">
        Select


      </button>
    </div>
  </div>
</template>

<script>
import { EmojiButton } from "@joeattardi/emoji-button";

export default {
  name: "EmojiInput",
  props: {
    modelValue: {
      type: String, // Changed to String to hold full content
      required: true,
    },
    options: {
      type: Object,
      default: () => ({ position: 'bottom' }), // Adjusted default
    },
  },
  mounted() {
    const picker = new EmojiButton(this.options);
    const btn = this.$refs.emojiBtn;

    picker.on("emoji", (emoji) => {
      // Append the new emoji to the current value
      const newValue = this.modelValue + emoji.emoji;
      this.$emit("update:modelValue", newValue);
    });

    btn.addEventListener("click", () => {
      picker.togglePicker(btn);
    });
  },
  methods: {
    updateInput(event) {
      // Update modelValue when typing
      this.$emit("update:modelValue", event.target.value);
    },
  },
};
</script>