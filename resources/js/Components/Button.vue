<template>
  <button :type="type" class="button">
    <slot/>
  </button>
</template>


<script setup>
defineProps({
  type: {
    type: String,
    default: 'submit',
  },
});
</script>

<style lang="scss" scoped>

@import 'resources/css/colors';

.button {
  display: inline-block;
  color: $white;
  font-size: 23px;
  font-weight: 600;
  padding: 20px 50px;
  background-color: $purple;
  border-radius: 23px;
  transition: all .3s ease;
  &:hover {
    transform: scale(1.05);
  }
}

</style>
