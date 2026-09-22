<script setup lang="ts">
import { ref } from 'vue'
import heroImg from '../assets/hero.png'
import viteLogo from '../assets/vite.svg'
import vueLogo from '../assets/vue.svg'

const count = ref(0)
</script>

<template>
  <section id="center" class="flex flex-col gap-[18px] md:gap-[25px] place-content-center place-items-center grow px-5 py-6 md:p-0">
    <div class="hero relative">
      <img :src="heroImg" class="base w-[170px] relative z-0 inset-x-0 mx-auto" width="170" height="179" alt="" />
      <img
        :src="vueLogo"
        alt="Vue logo"
        class="framework absolute z-[1] top-[34px] h-7 inset-x-0 mx-auto"
        style="transform: perspective(2000px) rotateZ(300deg) rotateX(44deg) rotateY(39deg) scale(1.4)"
      />
      <img
        :src="viteLogo"
        alt="Vite logo"
        class="vite absolute z-0 top-[107px] h-[26px] w-auto inset-x-0 mx-auto"
        style="transform: perspective(2000px) rotateZ(300deg) rotateX(40deg) rotateY(39deg) scale(0.8)"
      />
    </div>

    <div>
      <h1 class="font-medium text-[36px] md:text-[56px] tracking-[-1.68px] my-5 md:my-8 text-[color:var(--text-h)]">
        Get started
      </h1>
      <p>
        Edit
        <code class="inline-flex rounded text-[15px] leading-[135%] px-2 py-1 text-[color:var(--text-h)] bg-[color:var(--code-bg)]">src/app.vue</code>
        and save to test
        <code class="inline-flex rounded text-[15px] leading-[135%] px-2 py-1 text-[color:var(--text-h)] bg-[color:var(--code-bg)]">HMR</code>
      </p>
    </div>

    <button
      type="button"
      class="inline-flex text-base rounded-md px-2.5 py-[5px] mb-6 border-2 border-transparent transition-colors duration-300
             text-[color:var(--accent)] bg-[color:var(--accent-bg)]
             hover:border-[color:var(--accent-border)]
             focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-[color:var(--accent)]"
      @click="count++"
    >
      Count is {{ count }}
    </button>
  </section>

  <div class="ticks relative w-full before:content-[''] before:absolute before:top-[-4.5px] before:left-0 before:border-[5px] before:border-transparent before:border-l-[color:var(--border)] after:content-[''] after:absolute after:top-[-4.5px] after:right-0 after:border-[5px] after:border-transparent after:border-r-[color:var(--border)]"></div>

  <section id="next-steps" class="flex flex-col md:flex-row text-center md:text-left border-t border-[color:var(--border)]">
    <div id="docs" class="flex-1 p-6 md:p-8 border-b md:border-b-0 md:border-r border-[color:var(--border)]">
      <svg class="w-[22px] h-[22px] mb-4 mx-auto md:mx-0" role="presentation" aria-hidden="true">
        <use href="/icons.svg#documentation-icon"></use>
      </svg>
      <h2 class="font-medium text-xl md:text-2xl leading-[118%] tracking-[-0.24px] mb-2 text-[color:var(--text-h)]">Documentation</h2>
      <p>Your questions, answered</p>
      <ul class="flex flex-wrap justify-center md:justify-start gap-2 mt-5 md:mt-8">
        <li class="flex-1 basis-[calc(50%-8px)] md:flex-none">
          <a
            href="https://vite.dev/"
            target="_blank"
            class="w-full md:w-auto justify-center md:justify-start box-border flex items-center gap-2 rounded-md px-3 py-1.5 text-base no-underline transition-shadow duration-300 text-[color:var(--text-h)] bg-[color:var(--social-bg)] hover:shadow-[var(--shadow)]"
          >
            <img class="h-[18px]" :src="viteLogo" alt="" />
            Explore Vite
          </a>
        </li>
        <li class="flex-1 basis-[calc(50%-8px)] md:flex-none">
          <a
            href="https://vuejs.org/"
            target="_blank"
            class="w-full md:w-auto justify-center md:justify-start box-border flex items-center gap-2 rounded-md px-3 py-1.5 text-base no-underline transition-shadow duration-300 text-[color:var(--text-h)] bg-[color:var(--social-bg)] hover:shadow-[var(--shadow)]"
          >
            <img class="button-icon h-[18px] w-[18px]" :src="vueLogo" alt="" />
            Learn more
          </a>
        </li>
      </ul>
    </div>

    <div id="social" class="flex-1 p-6 md:p-8">
      <svg class="w-[22px] h-[22px] mb-4 mx-auto md:mx-0" role="presentation" aria-hidden="true">
        <use href="/icons.svg#social-icon"></use>
      </svg>
      <h2 class="font-medium text-xl md:text-2xl leading-[118%] tracking-[-0.24px] mb-2 text-[color:var(--text-h)]">Connect with us</h2>
      <p>Join the Vite community</p>
      <ul class="flex flex-wrap justify-center md:justify-start gap-2 mt-5 md:mt-8">
        <li class="flex-1 basis-[calc(50%-8px)] md:flex-none">
          <a href="https://github.com/vitejs/vite" target="_blank" class="w-full md:w-auto justify-center md:justify-start box-border flex items-center gap-2 rounded-md px-3 py-1.5 text-base no-underline transition-shadow duration-300 text-[color:var(--text-h)] bg-[color:var(--social-bg)] hover:shadow-[var(--shadow)]">
            <svg class="button-icon h-[18px] w-[18px]" role="presentation" aria-hidden="true"><use href="/icons.svg#github-icon"></use></svg>
            GitHub
          </a>
        </li>
        <li class="flex-1 basis-[calc(50%-8px)] md:flex-none">
          <a href="https://chat.vite.dev/" target="_blank" class="w-full md:w-auto justify-center md:justify-start box-border flex items-center gap-2 rounded-md px-3 py-1.5 text-base no-underline transition-shadow duration-300 text-[color:var(--text-h)] bg-[color:var(--social-bg)] hover:shadow-[var(--shadow)]">
            <svg class="button-icon h-[18px] w-[18px]" role="presentation" aria-hidden="true"><use href="/icons.svg#discord-icon"></use></svg>
            Discord
          </a>
        </li>
        <li class="flex-1 basis-[calc(50%-8px)] md:flex-none">
          <a href="https://x.com/vite_js" target="_blank" class="w-full md:w-auto justify-center md:justify-start box-border flex items-center gap-2 rounded-md px-3 py-1.5 text-base no-underline transition-shadow duration-300 text-[color:var(--text-h)] bg-[color:var(--social-bg)] hover:shadow-[var(--shadow)]">
            <svg class="button-icon h-[18px] w-[18px]" role="presentation" aria-hidden="true"><use href="/icons.svg#x-icon"></use></svg>
            X.com
          </a>
        </li>
        <li class="flex-1 basis-[calc(50%-8px)] md:flex-none">
          <a href="https://bsky.app/profile/vite.dev" target="_blank" class="w-full md:w-auto justify-center md:justify-start box-border flex items-center gap-2 rounded-md px-3 py-1.5 text-base no-underline transition-shadow duration-300 text-[color:var(--text-h)] bg-[color:var(--social-bg)] hover:shadow-[var(--shadow)]">
            <svg class="button-icon h-[18px] w-[18px]" role="presentation" aria-hidden="true"><use href="/icons.svg#bluesky-icon"></use></svg>
            Bluesky
          </a>
        </li>
      </ul>
    </div>
  </section>

  <div class="ticks relative w-full before:content-[''] before:absolute before:top-[-4.5px] before:left-0 before:border-[5px] before:border-transparent before:border-l-[color:var(--border)] after:content-[''] after:absolute after:top-[-4.5px] after:right-0 after:border-[5px] after:border-transparent after:border-r-[color:var(--border)]"></div>
  <section id="spacer" class="h-12 md:h-[88px] border-t border-[color:var(--border)]"></section>
</template>