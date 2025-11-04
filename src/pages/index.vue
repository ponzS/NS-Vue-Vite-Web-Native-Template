<script lang="ts" setup>
import Home from "@/components/Home.vue";
import Test from "./Test.vue";
// 使用模板中的 $navigateTo(Test) 进行原生端跳转；
// 在 Web 生成时由转换模块替换为 router.push('/Test')。
</script>

<template>
  <Frame>
    <Page class="bg-[#251353]">
      <ActionBar>
        <Label text="NativeScript for web" class="font-bold text-lg" />
      </ActionBar>

      <GridLayout rows="auto, *">
        <GridLayout row="1" rows="auto,*" class="p-4">
          <TabView >
            <TabViewItem title="Home">
              <Home />
            </TabViewItem>
            <TabViewItem title="Second">
              <StackLayout>
                <Label text="Second Tab Content" class="text-white" />
                <Button class="mt-4 p-3 border rounded text-white" @tap="$navigateTo(Test)">
                  Go To Test 
                </Button>
              </StackLayout>
            </TabViewItem>
            <TabViewItem title="Third">
              <Label text="Third Tab Content" class="text-white" />
            </TabViewItem>
          </TabView>
        </GridLayout>
      </GridLayout>
    </Page>
  </Frame>
</template>
