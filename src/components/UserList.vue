<template>
 

  <a-list item-layout="horizontal" :data-source="props.userList">

    <template #renderItem="{ item }">
      <a-list-item>
      
        <a-card hoverable style="width: 240px">
      <template #cover>
      <img alt="example" :src="gasket" />
    </template>
    <a-card-meta :title="item.userName">
      <template #description>{{item.userProfile }}</template>
    </a-card-meta>
    </a-card>
     
      </a-list-item>
    </template>
  </a-list>
</template>

<script setup lang="ts">
import gasket from "../assets/amiao.jpg";
import { withDefaults,defineProps } from "vue";
interface Props{
userList:any[]
}
const props=
  withDefaults(defineProps<Props>(),{
    userList:()=>[]
  }
)
</script>
<style scoped>
.gas {
  width: 200px;
}
</style>