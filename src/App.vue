<template>
  <div
    class="flex h-screen w-screen flex-col overflow-x-hidden bg-slate-50 text-black"
  >
    <nav
      class="sticky top-0 left-0 z-10 w-full flex-none border-b border-slate-900/10 bg-white/80 backdrop-blur"
    >
      <div class="max-w-8xl mx-auto">
        <div class="py-2 px-4">
          <div class="relative flex h-10 items-center">
            <a class="font-semibold text-black" href="/"
              ><img src="/images/logo.svg" width="140" height="40" alt="icon"
            /></a>
          </div>
        </div>
      </div>
    </nav>
    <div class="container mx-auto pb-10 pt-4">
      <div class="flex w-full flex-col gap-y-4">
        <div
          class="flex flex-col gap-y-4 p-4"
          v-for="(value, key) in data"
          :key="key"
        >
          <div class="text-lg font-semibold text-black">{{ key }}</div>
          <div class="grid grid-cols-2 gap-4 md:grid-cols-3 lg:grid-cols-4">
            <a v-for="item in value" :href="item.url">
              <div
                class="rounded-lg bg-white shadow-xl shadow-black/5 ring-1 ring-slate-700/10 h-full plausible-event-name=Tool+weekly-report"
              >
                <div class="group flex flex-col p-4">
                  <div class="flex items-center gap-2">
                    <span class="text-lg font-semibold text-black">{{
                      item.title
                    }}</span>
                  </div>
                  <span class="mt-4 text-sm text-gray-500">{{
                    item.desc
                  }}</span>
                </div>
              </div>
            </a>
          </div>
        </div>
      </div>
    </div>
    <!-- <footer class="mt-auto flex w-full justify-center py-4">
      <a href="https://beian.miit.gov.cn/" class="text-sm text-gray-400">沪ICP备19036898号-2</a>
    </footer> -->
  </div>
</template>

<script setup>
import data from "./data.json";
</script>
