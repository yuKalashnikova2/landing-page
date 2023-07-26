<script setup>
const props = defineProps({
  background: {
    type: String,
    default: false,
  },
  type: {
    type: String,
    default: 'button',
  },
  colorBtn: {
    type: String,
    default: 'light',
  },
  mobileWidth: {
    type: Boolean,
    default: false,
  },
})
</script>
<template>
  <button
    v-if="type === button"
    :class="[
      'btn',
      {
        'btn-primary': colorBtn === 'primary',
        'btn-secondary': colorBtn === 'secondary',
        'btn-light': colorBtn === 'light',
      },
    ]"
  >
    <slot></slot>
  </button>
  <NuxtLink
    v-else
    :to="to"
    :class="[
      'btn',
      {
        'btn-primary': colorBtn === 'primary',
        'btn-secondary': colorBtn === 'secondary',
        'btn-light': colorBtn === 'light',
        'btn-fullWidth': mobileWidth
      },
    ]"
    ><slot></slot
  ></NuxtLink>
</template>

<style lang="scss">
.btn {
  background: var(--black);
  color: #fff;
  display: inline-flex;
  justify-content: center;
  align-items: center;
  padding: 16px 32px;
  font-size: 16px;
  cursor: pointer;
  border: none;
  white-space: nowrap;
  @media screen and (max-width: 767px) {
    padding: 0 15px;
  }
  &:hover {
    opacity: 0.8;
  }
  &-primary {
    background: var(--black);
    color: #fff;
  }
  &-secondary {
    background: rgba(249, 249, 249, 0.15);
    color: #fff;
  }
  &-light {
    background: #f9f9f9;
    color: var(--black);
  }
  &-light {
    background: #f9f9f9;
    color: var(--black);
  }
  &-fullWidth {
    @media screen and (max-width: 767px) {
      width: 100%;
    }
  }
}
</style>
