<script setup>
import { onMounted, ref } from 'vue';

defineProps(['modelValue']);

defineEmits(['update:modelValue']);

const input = ref(null);

onMounted(() => {
  if (input.value.hasAttribute('autofocus')) {
    input.value.focus();
  }
});
</script>

<template>
  <input
    v-imask="mask"
    type="tel"
    @input="$emit('update:modelValue', $event.target.value)"
    ref="input"
  />
</template>

<script>
import { IMaskDirective } from 'vue-imask';

export default {
  data() {
    return {
      mask: {
        mask: '+{7}(000)000-00-00',
        lazy: true
      },
    }
  },
  directives: {
    imask: IMaskDirective
  },
}
</script>
