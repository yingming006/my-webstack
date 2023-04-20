<template>
  <!-- Card Section -->
  <div class="max-w-8xl px-4 py-10 space-y-8 sm:px-6 lg:px-8 lg:py-12">
    <div className="space-y-4" v-for="(value, key) in data" :key="key">
      <h2
        className="text-lg font-bold text-gray-900 dark:text-white sm:text-xl"
      >
        {{ key }}
      </h2>
      <!-- Grid -->
      <div class="grid sm:grid-cols-2 lg:grid-cols-6 gap-8 sm:gap-6">
        <!-- Card -->
        <a
          v-for="item in value"
          class="group flex flex-col bg-white border shadow-sm rounded-xl hover:shadow-md transition dark:bg-slate-900 dark:border-gray-800"
          :href="item.url"
        >
          <div class="p-4 md:p-5">
            <div class="flex">
              <div style="width: 40px; height: 40px">
                <img :src="item.icon" />
              </div>
              <div class="grow ml-5 text-left">
                <h3
                  class="group-hover:text-blue-600 font-semibold text-gray-800 dark:group-hover:text-gray-400 dark:text-gray-200"
                >
                  {{ item.title }}
                </h3>
                <p class="text-sm text-gray-500 line-clamp-1">
                  {{ item.desc }}
                </p>
              </div>
            </div>
          </div>
        </a>
        <!-- End Card -->
      </div>
      <!-- End Grid -->
    </div>
  </div>
  <!-- End Card Section -->
</template>

<script setup>
import data from "./data.json";
console.log(data);
</script>
