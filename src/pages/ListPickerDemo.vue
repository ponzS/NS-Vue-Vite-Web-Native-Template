<script lang="ts" setup>
import { Frame } from "@nativescript/core";
import { ref } from "nativescript-vue";
const items = ref(["Apple","Banana","Cherry"]);
const selectedIndex = ref(0);
function goBack() { Frame.goBack(); }
</script>

<template>
  <Page class="bg-[#251353]">
    <ActionBar>
      <NavigationButton text="Back" @tap="goBack" />
      <Label text="ListPicker" class="font-bold text-lg" />
    </ActionBar>
    <StackLayout class="p-6">
      <ListPicker :items="items" v-model:selectedIndex="selectedIndex" />
      <Label class="text-white mt-2" :text="`选择：${items[selectedIndex]}`" />
    </StackLayout>
  </Page>
</template>