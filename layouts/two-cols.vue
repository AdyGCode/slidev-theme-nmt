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
    class="slidev-layout two-columns"
    :class="props.layoutClass"
  >
    <div class="col-span-2" :class="props.class">
      <slot />
    </div>

    <div class="two-cols-left col-span-1 " :class="props.class">
      <slot name="left"/>
    </div>

    <div class="two-cols-right col-span-1 " :class="props.class">
      <slot name="right" />
    </div>
  </div>
</template>
