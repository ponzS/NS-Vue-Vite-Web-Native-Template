<script lang="ts" setup>
import { Frame } from "@nativescript/core";
function goBack() { Frame.goBack(); }
</script>

<template>
  <Page class="bg-[#251353]">
    <ActionBar>
      <NavigationButton text="Back" @tap="goBack" />
      <ActionItem text="Info" />
      <ActionItem text="Action" />
      <Label text="ActionBar" class="font-bold text-lg" />
    </ActionBar>
    <StackLayout class="p-6">
      <Label class="text-white" text="ActionBar 必须作为 Page 的直接子元素。" />
    </StackLayout>
  </Page>
</template>