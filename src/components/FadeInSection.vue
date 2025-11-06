<template>
  <div
    ref="el"
    class="transition-all duration-700 ease-out will-change-transform"
    :class="visible ? 'opacity-100 translate-y-0' : 'opacity-0 translate-y-6'"
  >
    <slot />
  </div>
</template>

<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue'

const el = ref(null)
const visible = ref(false)
let observer = null

onMounted(() => {
  observer = new IntersectionObserver(
    entries => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          visible.value = true
          if (observer) observer.disconnect()
        }
      })
    },
    { threshold: 0.2 }
  )

  if (el.value) observer.observe(el.value)
})

onBeforeUnmount(() => {
  if (observer) observer.disconnect()
})
</script>
