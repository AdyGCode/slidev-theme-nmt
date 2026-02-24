<template>
  <div class="slidev-layout default h-full">
    <slot />
    <ImageWithOptionalCaption
      class="h-5/6 p-4"
      :caption="imageCaption"
      :footnoteNumber="imageFootnoteNumber"
      :url="imageUrl"
    />
  </div>
</template>

<script setup lang="ts">

defineProps<{
  imageCaption?: string;
  imageFootnoteNumber?: number;
  imageUrl: string;
}>();
</script>
