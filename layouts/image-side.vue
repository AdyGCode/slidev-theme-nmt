<template>
  <div class="flex h-full">
    <div class="slidev-layout default flex-1">
      <slot />
    </div>
    <ImageWithOptionalCaption
      class="flex-1 h-4/5 m-auto px-4"
      :class="{
        'order-first': imageX === 'l',
      }"
      :caption="imageCaption"
      :footnoteNumber="imageFootnoteNumber"
      :url="imageUrl"
    />
  </div>
</template>

<script setup lang="ts">
withDefaults(
  defineProps<{
    imageCaption?: string;
    imageFootnoteNumber?: number;
    imageUrl: string;
    imageX?: 'l' | 'r';
  }>(),
  { imageX: 'r' },
);
</script>
