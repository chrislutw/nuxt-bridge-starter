<script setup lang="ts">
const mouseItem = useMouse()
const source = ref('hi this is copy string')
const { text, copy, copied, isSupported } = useClipboard({ source })
</script>
<template>
  <div
    text="xl gray4" m-5
    flex
    justify-center
    gap-3
  >
    <NuxtLink i-carbon-campsite to="/" />
    <a i-carbon-logo-github href="https://github.com/antfu/vitesse-nuxt" target="__blank" />
    <DarkToggle />
    <!-- {{ mouseItem }} -->
    {{ text }}
    {{ copied }}
    is supported:{{ isSupported }}
    <button type="submit" class="mx-auto my-3 text-sm block btn" @click="copy()">
      GO
    </button>
  </div>
</template>
