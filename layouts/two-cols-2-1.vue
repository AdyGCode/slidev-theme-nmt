<script setup lang="ts">
const props = defineProps({
  class: {
    type: String,
  },
  layoutClass: {
    type: String,
  },
});
</script>

<template>
  <div
    class="slidev-layout two-columns two-one"
    :class="props.layoutClass"
  >
    <div class="col-span-2 two-one" :class="props.class">
      <slot />
    </div>

    <div class="col-span-1 two-one" :class="props.class">
      <slot name="right" />
    </div>
  </div>
</template>
