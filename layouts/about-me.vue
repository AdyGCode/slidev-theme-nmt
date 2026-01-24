<script setup lang="ts">
  import { computed } from 'vue'
  import { handleBackground } from '@slidev/client/layoutHelper.ts'

  const props = defineProps<{
    imageSrc?: string
    helloMsg?: string
    name?: string
    company?: string
    jobRole?: string
    subjects?: string
    skills?: string
    email?: string
    msTeams?: string
    website?: string
    github?: string
    position?: string
  }>()

  const style = computed(() => handleBackground(props.imageSrc, false, 'fit'))
  const flexRow = computed(() => props.position === 'left' ? 'flex-row-reverse' : 'flex-row')
  const textItems = computed(() => props.position === 'left' ? 'items-start' : 'items-end')
  const textAlign = computed(() => props.position === 'left' ? 'text-left' : 'text-right')
</script>

<template>
  <div class="slidev-layout about-me p-0">
    <div class="flex h-full" :class="flexRow">
      <div class="w-1/2 h-full flex flex-col justify-end bg-contain" :style="style">
      </div>

      <div class="w-1/2 flex flex-col justify-between px-8 pt-8" :class="textItems">
        <h1 v-if="helloMsg" class="flex">{{ helloMsg }}</h1>

        <div class="flex flex-col flex flex-col justify-end py-16" :class="[textItems, textAlign]">
          <h2 class="font-extrabold">{{ name }}</h2>

          <dl class="text-2xl mt-4 flex flex-wrap gap-0">
            <dt v-if="company" class="w-1/10"><fa7-solid-building class="text-zinc-600" /></dt>
            <dd v-if="company" class="w-9/10 company">{{ company }}</dd>

            <dt v-if="jobRole" class="w-1/10"><fa7-solid-user-circle class="text-zinc-600" /></dt>
            <dd v-if="jobRole" class="w-9/10 line-1">{{ jobRole }}</dd>

            <dt v-if="subjects" class="w-1/10"><fa7-solid-book-skull class="text-zinc-600" /></dt>
            <dd v-if="subjects" class="w-9/10 line-2">{{ subjects }}</dd>

            <dt v-if="skills" class="w-1/10"><fa7-solid-laptop-file class="text-zinc-600" /></dt>
            <dd v-if="skills" class="w-9/10 line-3">{{ skills }}</dd>
          </dl>

          <dl class="text-2xl mt-4 flex flex-wrap gap-0">
            <dt v-if="email" class="w-1/10"><fa7-solid-envelope class="text-zinc-600" /></dt>
            <dd v-if="email" class="w-9/10 grow email ">{{ email }}</dd>

            <dt v-if="msTeams" class="w-1/10"><fa7-brands-microsoft class="text-zinc-600" /></dt>
            <dd v-if="msTeams" class="w-9/10 grow social social-1">{{ msTeams }}</dd>

            <dt v-if="website" class="w-1/10"><fa7-solid-globe class="text-zinc-600" /></dt>
            <dd v-if="website" class="w-9/10 grow social social-2">{{ website }}</dd>

            <dt v-if="github" class="w-1/10"><fa7-brands-github class="text-zinc-600" /></dt>
            <dd v-if="github" class="w-9/10 grow social social-3">{{ github }}</dd>
          </dl>
        </div>
      </div>
    </div>

    <slot />
  </div>
</template>

