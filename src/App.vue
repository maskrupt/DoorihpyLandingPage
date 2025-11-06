<template>
  <div class="min-h-screen bg-slate-950 text-slate-50">
    <!-- NAVBAR -->
    <header class="sticky top-0 z-20 border-b border-slate-900/70 bg-slate-950/85 backdrop-blur">
      <div class="mx-auto flex max-w-6xl items-center justify-between px-4 py-3">
        <div class="flex items-center gap-2">
          <div
            class="flex h-9 w-9 items-center justify-center rounded-2xl border border-sky-500/50 bg-sky-500/10"
          >
            <span class="text-xl font-black text-sky-400">D</span>
          </div>
          <div class="text-lg font-semibold tracking-tight">Dooriphy</div>
        </div>

        <nav class="hidden gap-6 text-sm text-slate-300 md:flex">
          <a href="#offer" class="hover:text-white">What we offer</a>
          <a href="#why" class="hover:text-white">Why Dooriphy</a>
          <a href="#contact" class="hover:text-white">Contact</a>
        </nav>

        <div class="hidden text-[0.7rem] text-slate-500 sm:block">
          Copyright MaskRupt. Do not distribute!
        </div>
      </div>
    </header>

    <main>
      <!-- HERO -->
      <section
        class="relative overflow-hidden border-b border-slate-900/70 bg-gradient-to-br from-slate-950 via-slate-900 to-slate-950"
      >
        <div class="pointer-events-none absolute inset-0 opacity-40">
          <div
            class="absolute -left-40 top-0 h-80 w-80 rounded-full bg-sky-500/25 blur-3xl"
          ></div>
          <div
            class="absolute bottom-0 right-0 h-96 w-96 rounded-full bg-emerald-500/15 blur-3xl"
          ></div>
        </div>

        <div
          class="relative mx-auto flex justify-between max-w-6xl flex-col items-center gap-10 px-4 py-16 md:flex-row md:py-20"
        >
          <!-- Hero text -->
          <FadeInSection class="max-w-xl space-y-6 flex-shrink-0">
            <p
              class="inline-flex items-center gap-2 rounded-full border border-sky-500/30 bg-sky-500/10 px-3 py-1 text-[0.7rem] font-medium uppercase tracking-[0.2em] text-sky-300"
            >
              Room signage • Office 365 • Real-time
            </p>

            <h1
              class="text-balance text-4xl font-extrabold tracking-tight text-white sm:text-5xl md:text-6xl"
            >
              Meetings that stay
              <span
                class="bg-gradient-to-r from-sky-400 via-sky-300 to-emerald-300 bg-clip-text text-transparent"
              >
                in sync
              </span>
              on every door.
            </h1>

            <p class="text-sm leading-relaxed text-slate-300 sm:text-base">
              Dooriphy turns your Office 365 room calendars into live door
              displays. Every board room, huddle space and focus booth shares
              the same source of truth&mdash;with zero extra apps for your team.
            </p>

            <div class="flex flex-wrap items-center gap-3">
              <a
                href="#offer"
                class="inline-flex items-center gap-2 rounded-xl bg-sky-500 px-4 py-2 text-sm font-semibold text-slate-950 shadow-lg shadow-sky-500/40 hover:bg-sky-400"
              >
                Explore what we offer
                <span aria-hidden="true">↘</span>
              </a>
              <span class="text-xs text-slate-400">
                Designed for tablets, kiosks and wall screens.
              </span>
            </div>
          </FadeInSection>

          <!-- Hero animated screen -->
          <FadeInSection>
            <HeroScreenCarousel />
          </FadeInSection>
        </div>
      </section>

      <!-- WHAT WE OFFER -->
      <section id="offer" class="border-b border-slate-900/70 bg-slate-950">
        <div class="mx-auto max-w-6xl px-4 py-14">
          <FadeInSection>
            <div class="max-w-2xl">
              <h2 class="text-2xl font-semibold tracking-tight text-white sm:text-3xl">
                What Dooriphy offers.
              </h2>
              <p class="mt-2 text-sm text-slate-300 sm:text-base">
                A single, focused product: real-time room signage built for
                Office 365 calendars and modern meeting spaces.
              </p>
            </div>
          </FadeInSection>

          <div class="mt-8 grid gap-6 md:grid-cols-3">
            <FadeInSection>
              <article class="rounded-2xl border border-slate-800 bg-slate-900/70 p-5">
                <h3 class="text-sm font-semibold text-sky-300">
                  Live room status on every screen
                </h3>
                <p class="mt-2 text-xs text-slate-300">
                  Instantly see if a room is free, busy or about to be used.
                  Dooriphy listens to your Office 365 room calendars and updates
                  each display in seconds &mdash; no manual refresh.
                </p>
              </article>
            </FadeInSection>

            <FadeInSection>
              <article class="rounded-2xl border border-slate-800 bg-slate-900/70 p-5">
                <h3 class="text-sm font-semibold text-sky-300">
                  Multi-calendar, one backend
                </h3>
                <p class="mt-2 text-xs text-slate-300">
                  Connect multiple room mailboxes (Board Room A, B, focus rooms)
                  into a single backend. Each screen subscribes to its own room,
                  but they all share the same core logic and security.
                </p>
              </article>
            </FadeInSection>

            <FadeInSection>
              <article class="rounded-2xl border border-slate-800 bg-slate-900/70 p-5">
                <h3 class="text-sm font-semibold text-sky-300">
                  Organizer & meeting notes at the door
                </h3>
                <p class="mt-2 text-xs text-slate-300">
                  Surface the organizer, meeting title and notes directly on the
                  display, so everyone knows who booked the room and what it’s
                  for &mdash; without opening Outlook.
                </p>
              </article>
            </FadeInSection>
          </div>

          <div class="mt-6 grid gap-6 md:grid-cols-2">
            <FadeInSection>
              <article class="rounded-2xl border border-slate-800 bg-slate-900/70 p-5">
                <h3 class="text-sm font-semibold text-sky-300">
                  Kiosk mode & wall-mounted tablets
                </h3>
                <p class="mt-2 text-xs text-slate-300">
                  Designed for always-on devices: Chrome kiosk mode, Electron,
                  iOS/Android tablets or mini-PCs behind the screen. Large
                  typography, minimal controls and subtle animations keep it
                  readable from the hallway.
                </p>
              </article>
            </FadeInSection>

            <FadeInSection>
              <article class="rounded-2xl border border-slate-800 bg-slate-900/70 p-5">
                <h3 class="text-sm font-semibold text-sky-300">
                  Secure Microsoft sign-in
                </h3>
                <p class="mt-2 text-xs text-slate-300">
                  A simple splash screen with QR code lets an authorized user sign
                  in with Microsoft once. Dooriphy then uses secure application
                  permissions to read room calendars, while screens use a token
                  broadcast over SignalR.
                </p>
              </article>
            </FadeInSection>
          </div>
        </div>
      </section>

      <!-- WHY CHOOSE US -->
      <section id="why" class="border-b border-slate-900/70 bg-slate-950">
        <div class="mx-auto max-w-6xl px-4 py-14">
          <FadeInSection>
            <div class="max-w-2xl">
              <h2 class="text-2xl font-semibold tracking-tight text-white sm:text-3xl">
                Why teams choose Dooriphy.
              </h2>
              <p class="mt-2 text-sm text-slate-300 sm:text-base">
                Plenty of tools book rooms. Dooriphy focuses on one thing: making
                your room availability obvious at a glance.
              </p>
            </div>
          </FadeInSection>

          <div class="mt-8 grid gap-6 md:grid-cols-3">
            <FadeInSection>
              <div class="flex flex-col gap-2 rounded-2xl border border-slate-800 bg-slate-900/70 p-5">
                <div class="text-sm font-semibold text-emerald-300">Less hallway chaos</div>
                <p class="text-xs text-slate-300">
                  When every door clearly shows whether it’s free or booked, there
                  are fewer interruptions, knock-ins and “is someone using this?”
                  moments.
                </p>
              </div>
            </FadeInSection>

            <FadeInSection>
              <div class="flex flex-col gap-2 rounded-2xl border border-slate-800 bg-slate-900/70 p-5">
                <div class="text-sm font-semibold text-emerald-300">Native to Microsoft 365</div>
                <p class="text-xs text-slate-300">
                  No new booking app. Your existing Outlook / Teams meetings drive
                  the displays. Dooriphy simply visualizes the truth that already
                  lives in Office 365.
                </p>
              </div>
            </FadeInSection>

            <FadeInSection>
              <div class="flex flex-col gap-2 rounded-2xl border border-slate-800 bg-slate-900/70 p-5">
                <div class="text-sm font-semibold text-emerald-300">Simple to deploy</div>
                <p class="text-xs text-slate-300">
                  One .NET backend and lightweight Vue frontends. Point devices at
                  the URL, lock them into kiosk mode, and you’re done.
                </p>
              </div>
            </FadeInSection>
          </div>

          <FadeInSection>
            <div class="mt-8 rounded-2xl border border-slate-800 bg-slate-900/80 p-5 text-xs text-slate-300">
              <h3 class="mb-2 text-sm font-semibold text-sky-200">
                Multi-calendar in one application, explained:
              </h3>
              <ul class="space-y-2">
                <li>
                  • IT maps each room mailbox or category (e.g.
                  <span class="font-mono">BoardRoomA@</span>,
                  <span class="font-mono">BoardRoomB@</span>) into Dooriphy.
                </li>
                <li>
                  • Dooriphy subscribes to calendar changes using Microsoft Graph application permissions.
                </li>
                <li>
                  • Each screen connects to its room channel in SignalR, receiving only the events that matter.
                </li>
                <li>
                  • All views (today, upcoming, timeline bar) are rendered from the same normalized appointments.
                </li>
              </ul>
            </div>
          </FadeInSection>
        </div>
      </section>

      <!-- CONTACT FORM -->
      <section
        id="contact"
        class="border-b border-slate-900/70 bg-gradient-to-br from-slate-950 via-slate-900 to-slate-950"
      >
        <div class="mx-auto max-w-6xl px-4 py-14">
          <FadeInSection>
            <div class="max-w-xl">
              <h2 class="text-2xl font-semibold tracking-tight text-white sm:text-3xl">
                Get in touch about Dooriphy.
              </h2>
              <p class="mt-2 text-sm text-slate-300 sm:text-base">
                Interested in piloting Dooriphy in your office, or have questions
                about integrating with your existing Microsoft 365 setup?
                Drop us a note.
              </p>
            </div>
          </FadeInSection>

          <div class="mt-8 grid gap-8 md:grid-cols-[1.2fr,0.8fr]">
            <!-- FORM -->
            <FadeInSection>
              <form
                @submit.prevent="handleSubmit"
                class="space-y-4 rounded-2xl border border-slate-800 bg-slate-900/75 p-5"
              >
                <div class="grid gap-4 sm:grid-cols-2">
                  <div>
                    <label class="block text-xs font-semibold text-slate-300 mb-1">
                      Name
                    </label>
                    <input
                      v-model="form.name"
                      type="text"
                      class="w-full rounded-lg border border-slate-700 bg-slate-950/60 px-3 py-2 text-sm text-slate-50 outline-none focus:border-sky-500 focus:ring-1 focus:ring-sky-500"
                      placeholder="Your name"
                    />
                  </div>
                  <div>
                    <label class="block text-xs font-semibold text-slate-300 mb-1">
                      Company
                    </label>
                    <input
                      v-model="form.company"
                      type="text"
                      class="w-full rounded-lg border border-slate-700 bg-slate-950/60 px-3 py-2 text-sm text-slate-50 outline-none focus:border-sky-500 focus:ring-1 focus:ring-sky-500"
                      placeholder="Company or team"
                    />
                  </div>
                </div>

                <div>
                  <label class="block text-xs font-semibold text-slate-300 mb-1">
                    Email
                  </label>
                  <input
                    v-model="form.email"
                    type="email"
                    class="w-full rounded-lg border border-slate-700 bg-slate-950/60 px-3 py-2 text-sm text-slate-50 outline-none focus:border-sky-500 focus:ring-1 focus:ring-sky-500"
                    placeholder="you@company.com"
                  />
                </div>

                <div>
                  <label class="block text-xs font-semibold text-slate-300 mb-1">
                    Message
                  </label>
                  <textarea
                    v-model="form.message"
                    rows="4"
                    class="w-full rounded-lg border border-slate-700 bg-slate-950/60 px-3 py-2 text-sm text-slate-50 outline-none focus:border-sky-500 focus:ring-1 focus:ring-sky-500"
                    placeholder="Tell us about your rooms, calendars, and what you want Dooriphy to solve."
                  ></textarea>
                </div>

                <p v-if="error" class="text-xs text-red-400">
                  {{ error }}
                </p>
                <p v-if="success" class="text-xs text-emerald-400">
                  Thanks! Your message has been captured (demo only).
                </p>

                <button
                  type="submit"
                  :disabled="submitting"
                  class="inline-flex items-center gap-2 rounded-xl bg-sky-500 px-4 py-2 text-sm font-semibold text-slate-950 shadow-lg shadow-sky-500/40 hover:bg-sky-400 disabled:cursor-not-allowed disabled:opacity-60"
                >
                  <span v-if="!submitting">Send message</span>
                  <span v-else>Sending…</span>
                </button>
              </form>
            </FadeInSection>

            <!-- SIDE INFO -->
            <FadeInSection>
              <div
                class="rounded-2xl border border-slate-800 bg-slate-900/60 p-5 text-xs text-slate-300"
              >
                <h3 class="text-sm font-semibold text-sky-200 mb-2">
                  What to include:
                </h3>
                <ul class="space-y-2">
                  <li>• How many rooms and locations you have.</li>
                  <li>• Whether you already use Office 365 room mailboxes.</li>
                  <li>• What devices you plan to mount at the doors.</li>
                  <li>• Any custom branding or features you care about.</li>
                </ul>
                <p class="mt-4 text-[0.7rem] text-slate-500">
                  This demo landing page doesn’t send real email yet. In a live
                  deployment, this form can post to an API, send to an inbox, or
                  create tickets in your support system.
                </p>
                <p class="mt-6 text-[0.7rem] text-slate-500">
                  Copyright MaskRupt. Do not distribute!
                </p>
              </div>
            </FadeInSection>
          </div>
        </div>
      </section>

      <!-- FOOTER -->
      <footer class="bg-slate-950">
        <div
          class="mx-auto flex max-w-6xl flex-col items-center justify-between gap-2 border-t border-slate-900 px-4 py-4 text-[0.75rem] text-slate-500 sm:flex-row"
        >
          <span>© {{ year }} MaskRupt. Dooriphy.</span>
          <span class="text-[0.7rem]"
            >Room signage for Office 365 multi-calendar environments.</span
          >
        </div>
      </footer>
    </main>
  </div>
</template>

<script setup>
import { reactive, ref, computed } from 'vue'
import FadeInSection from './components/FadeInSection.vue'
import HeroScreenCarousel from './components/HeroScreenCarousel.vue'

const form = reactive({
  name: '',
  company: '',
  email: '',
  message: '',
})

const submitting = ref(false)
const error = ref('')
const success = ref(false)

const year = computed(() => new Date().getFullYear())

function handleSubmit() {
  error.value = ''
  success.value = false

  if (!form.name || !form.email || !form.message) {
    error.value = 'Please fill in your name, email and a short message.'
    return
  }

  submitting.value = true

  // Fake async submit
  setTimeout(() => {
    submitting.value = false
    success.value = true
  }, 800)
}
</script>
