<script lang="ts" setup>
import { Frame } from "@nativescript/core";
import { ref } from "nativescript-vue";
const val = ref(30);
function goBack() { Frame.goBack(); }
</script>

<template>
  <Page class="bg-[#251353]">
    <ActionBar>
      <NavigationButton text="Back" @tap="goBack" />
      <Label text="Progress" class="font-bold text-lg" />
    </ActionBar>
    <StackLayout class="p-6">
      <Progress :value="val" :max="100" />
      <Slider v-model:value="val" :min="0" :max="100" class="mt-2" />
      <Label class="text-white mt-2" :text="`进度：${val}%`" />
    </StackLayout>
  </Page>
</template>