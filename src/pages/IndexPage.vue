<template>
  <div class="index-page">
    <a-input-search
      v-model:value="searchText"
      placeholder="input search text"
      enter-button="Search"
      size="large"
      @search="onSearch"
    />
    <a-tabs v-model:activeKey="activeKey">
      <a-tab-pane key="1" tab="Tab 1">
        <PostList />
      </a-tab-pane>
      <a-tab-pane key="2" tab="Tab 2" force-render
        >Content of Tab Pane 2
      </a-tab-pane>
      <a-tab-pane key="3" tab="Tab 3">Content of Tab Pane 3</a-tab-pane>
    </a-tabs>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";
import PostList from "@/components/PostList.vue";

const searchText = ref("");
const activeKey = ref("1");
const onSearch = (searchValue: string) => {
  console.log("use value", searchValue);
  console.log("or use this.value", searchText.value);
};
</script>
