<script lang="ts" setup>
import { Frame, Label } from "@nativescript/core";
function goBack() { Frame.goBack(); }
function onCreatingView(args: any) {
  const lbl = new Label();
  lbl.text = 'Native Placeholder 已创建';
  args.view = lbl;
}
</script>

<template>
  <Page class="bg-[#251353]">
    <ActionBar>
      <NavigationButton text="Back" @tap="goBack" />
      <Label text="Placeholder" class="font-bold text-lg" />
    </ActionBar>
    <StackLayout class="p-6">
      <Placeholder :creatingView="onCreatingView" />
      <Label class="text-white mt-2" text="Web端 Placeholder 为空容器" />
    </StackLayout>
  </Page>
</template>