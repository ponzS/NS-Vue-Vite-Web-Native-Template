<script lang="ts" setup>
import { Frame } from "@nativescript/core";
import { ref } from "nativescript-vue";
const text = ref("Multiline Text\n第二行");
function goBack() { Frame.goBack(); }
</script>

<template>
  <Page class="bg-[#251353]">
    <ActionBar>
      <NavigationButton text="Back" @tap="goBack" />
      <Label text="TextView" class="font-bold text-lg" />
    </ActionBar>
    <StackLayout class="p-6">
      <TextView v-model:text="text" />
      <Label class="text-white mt-2" :text="`文本：${text}`" />
    </StackLayout>
  </Page>
</template>