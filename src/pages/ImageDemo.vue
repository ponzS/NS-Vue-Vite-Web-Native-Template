<script lang="ts" setup>
import { Frame } from "@nativescript/core";
function goBack() { Frame.goBack(); }
</script>

<template>
  <Page class="bg-[#251353]">
    <ActionBar>
      <NavigationButton text="Back" @tap="goBack" />
      <Label text="Image" class="font-bold text-lg" />
    </ActionBar>
    <StackLayout class="p-6">
      <Image src="https://picsum.photos/200" class="mt-2" />
      <Label class="text-white mt-2" text="随机占位图（可能因网络而变化）" />
    </StackLayout>
  </Page>
</template>