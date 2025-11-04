<script lang="ts" setup>
import { Frame } from "@nativescript/core";
import { ref } from "nativescript-vue";
const dateVal = ref<Date>(new Date());
function goBack() { Frame.goBack(); }
</script>

<template>
  <Page class="bg-[#251353]">
    <ActionBar>
      <NavigationButton text="Back" @tap="goBack" />
      <Label text="DatePicker" class="font-bold text-lg" />
    </ActionBar>
    <StackLayout class="p-6">
      <DatePicker v-model:date="dateVal" class="mt-2" />
      <Label class="text-white mt-2" :text="`日期：${dateVal?.toDateString?.()}`" />
    </StackLayout>
  </Page>
</template>