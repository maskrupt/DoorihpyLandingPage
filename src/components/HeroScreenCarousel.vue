<template>
  <div class="relative w-full max-w-md">
    <div
      class="relative mx-auto max-w-[calc(30rem*4/5)] w-[calc(30rem*4/5)] overflow-hidden rounded-3xl border border-sky-500/30 bg-slate-900/70 shadow-xl shadow-slate-950/60"
    >
      <div
        class="flex items-center justify-between px-4 py-3 text-xs text-slate-300/90"
      >
        <span class="font-semibold text-sky-300">{{ current.roomName }}</span>
        <span class="font-mono text-[0.65rem] text-slate-400">
          {{ current.clock }}
        </span>
      </div>

      <div class="px-4 pt-1">
        <!-- status pill -->
        <div
          class="inline-flex items-center gap-2 rounded-full px-3 py-1 text-[0.7rem]"
          :class="current.pillClass"
        >
          <span
            class="h-2 w-2 rounded-full shadow-[0_0_0_4px_rgba(15,23,42,0.65)]"
            :class="current.dotClass"
          ></span>
          {{ current.statusLabel }}
        </div>
      </div>

      <!-- animated content -->
      <div class="relative mt-4 flex-1 px-4 pb-4">
        <transition name="fade-slide" mode="out-in">
          <div :key="current.id" class="space-y-3">
            <div class="text-sm text-slate-300">
              <span class="font-semibold text-slate-50">
                {{ current.headline }}
              </span>
            </div>
            <p class="text-xs text-slate-400">
              {{ current.subline }}
            </p>

            <div class="mt-3 h-px w-full bg-slate-800/80"></div>

            <div class="space-y-1 text-xs text-slate-300">
              <div>
                <span class="font-semibold text-slate-100">Now:</span>
                <span class="ml-1 text-sky-100">{{ current.nowLabel }}</span>
              </div>
              <div>
                <span class="font-semibold text-slate-100">Next:</span>
                <span class="ml-1 text-slate-200">{{ current.nextLabel }}</span>
              </div>
              <div class="text-slate-400">
                {{ current.footer }}
              </div>
            </div>
          </div>
        </transition>
      </div>

      <!-- timeline bar -->
      <div class="px-4 pb-4">
        <div class="flex items-center justify-between text-[0.65rem] text-slate-500">
          <span>Now</span>
          <span>{{ current.range }}</span>
        </div>
        <div class="mt-1 h-1.5 rounded-full bg-slate-800/80 overflow-hidden">
          <div
            class="h-full rounded-full transition-all duration-700"
            :class="current.progressClass"
            :style="{ width: current.progress + '%' }"
          ></div>
        </div>
      </div>
    </div>

    <!-- floating label -->
    <div
      class="pointer-events-none absolute -right-4 -top-10 rounded-2xl border border-emerald-400/40 bg-emerald-500/10 px-3 py-2 text-[0.7rem] text-emerald-100 shadow-lg shadow-emerald-500/25"
    >
      <div class="font-semibold">Live Dooriphy preview</div>
      <div class="text-emerald-200/80">
        Screens cycle through Free, Upcoming and Busy.
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, computed, onMounted, onBeforeUnmount } from 'vue'

const screens = [
  {
    id: 'free',
    roomName: 'Board Room A',
    clock: '09:42 • Tue',
    statusLabel: 'Free for the rest of the morning',
    pillClass: 'bg-emerald-500/10 text-emerald-200',
    dotClass: 'bg-emerald-300',
    headline: 'Walk up and use the room.',
    subline: 'No more bookings until after lunch.',
    nowLabel: 'Room is available',
    nextLabel: 'Design Review — 13:00–14:00',
    footer: 'Ideal for ad-hoc meetings, stand-ups or quick calls.',
    range: '09:00 — 12:00',
    progressClass: 'bg-emerald-400',
    progress: 25,
  },
  {
    id: 'upcoming',
    roomName: 'Board Room A',
    clock: '11:52 • Tue',
    statusLabel: 'Starts in 8 minutes',
    pillClass: 'bg-amber-500/10 text-amber-200',
    dotClass: 'bg-amber-300',
    headline: 'Weekly Sync — Product',
    subline: 'Dooriphy shows a warm warning before the next booking.',
    nowLabel: 'Free until 12:00',
    nextLabel: 'Weekly Sync — Product 12:00–13:00',
    footer: 'Teams see the countdown and avoid starting long meetings.',
    range: '11:00 — 12:00',
    progressClass: 'bg-amber-400',
    progress: 80,
  },
  {
    id: 'busy',
    roomName: 'Board Room A',
    clock: '12:21 • Tue',
    statusLabel: 'Busy until 13:00',
    pillClass: 'bg-sky-500/10 text-sky-200',
    dotClass: 'bg-sky-300',
    headline: 'Hello World till 13:00',
    subline: 'Organizer and notes appear directly on the display.',
    nowLabel: 'Hello World — Planning',
    nextLabel: 'Focus Time block 13:15–14:00',
    footer: 'Keeps walk-ups informed without opening Outlook.',
    range: '12:00 — 13:00',
    progressClass: 'bg-sky-400',
    progress: 40,
  },
]

const index = ref(0)
const current = computed(() => screens[index.value])
let timer

onMounted(() => {
  timer = setInterval(() => {
    index.value = (index.value + 1) % screens.length
  }, 7000)
})

onBeforeUnmount(() => {
  if (timer) clearInterval(timer)
})
</script>

<style scoped>
.fade-slide-enter-active,
.fade-slide-leave-active {
  transition: all 0.5s ease;
}
.fade-slide-enter-from {
  opacity: 0;
  transform: translateY(8px);
}
.fade-slide-leave-to {
  opacity: 0;
  transform: translateY(-8px);
}
</style>
