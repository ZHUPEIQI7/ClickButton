<template>
  <div class="home">

    <button id="button1" ref="target" @click="openNewPage">打开新页面</button>

  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src
import wnsdk from "@tjmt/wnsdk";

@Component

export default class Home extends Vue {

  private openNewPage() {
    wnsdk.page.open({
      url: "http://www.tjmeiteng.com",
      data: {},
      needCode: 0, 
      success(result:any) {
        console.log(11111111111111)
      },
      error(error:any) {
        // 失败处理...
      }
    })
  }

}
</script>

<style scoped lang="scss">
  
</style>
