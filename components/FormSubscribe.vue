<script setup>
   const props = defineProps({
  differentColor: {
    type: String,
    required: false,
  },
  bgColorInput: {
    type: String,
    required: false,
  },
  bgColorInputText: {
    type: String,
    required: false,
  }
})

</script>
<template>
    <form class="subscribe-form">
        <input
          type="text"
          placeholder="your@email.com"
          class="input-text subscribe-form__input"
          :style="{backgroundColor: bgColorInput, color: bgColorInputText}"
        />
        <ButtonUI :color-btn="differentColor || 'primary'">Sign up</ButtonUI>
    </form>
      
</template>

<style lang="scss">
    .subscribe-form {
        display: flex;
        &__input {
            flex-grow: 1;
        }
        
    }
</style>