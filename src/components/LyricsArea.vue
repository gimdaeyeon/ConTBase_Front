<template>
  <div class="layout-content-container flex flex-col w-[360px]">
    <div class="pb-3">
      <div class="flex border-b border-gray-200 px-4 gap-8">
        <a class="flex flex-col items-center justify-center border-b-[3px] border-b-[#00AB6B] text-[#1C160C] pb-[13px] pt-4"
           href="#">
          <p class="text-[#1C160C] text-sm font-bold leading-normal tracking-[0.015em]">Lyrics</p>
        </a>
        <a class="flex flex-col items-center justify-center border-b-[3px] border-b-transparent text-[#A18249] pb-[13px] pt-4"
           href="#">
          <p class="text-[#B88746] text-sm font-bold leading-normal tracking-[0.015em]">Settings</p>
        </a>
      </div>
    </div>
    <div class="flex max-w-[480px] flex-wrap items-end gap-4 px-4 py-3 h-full">
      <label class="flex flex-col min-w-40 flex-1 h-full">
                <TextArea
                    placeholder="Type or paste lyrics here..."
                    class="form-input flex w-full min-w-0 flex-1 resize-none overflow-y-scroll rounded-xl focus:outline-0 focus:ring-0 border
                    border-gray-200 bg-[#FFFFFF] focus:border-[#E9DFCE] h-full min-h-36 placeholder:text-[#B88746] p-[15px] text-base font-normal leading-normal"
                    v-model="lyrics"
                ></TextArea>
      </label>
    </div>
  </div>
</template>

<script setup>

import TextArea from "@/components/common/tag/TextArea.vue";
import {useLyrics} from "@/store/useLyrics.js";
import {storeToRefs} from "pinia";

const lyricsStore = useLyrics();
const {lyrics} = storeToRefs(lyricsStore);


</script>

<style scoped>

</style>