<template>
  <div class="song_wrapper" ref="wrapper">
    <ul class="song_list">
      <li v-for="(item, index) in list" :key="index" @click="liClick(item.id)">{{ item.name }} </li>
      <!-- <li>岁月神偷--金玟岐</li>
            <li>岁月神偷--汪苏泷</li>
            <li>岁月神偷--不才</li>
            <li>岁月神偷（磁性男声版）（Cover：金玟岐）--于大海（于黑蛋）</li> -->
    </ul>
  </div>
</template>

<script>
import iscroll from "iscroll";
export default {
  data() {
    return {
      list: [],
      myscroll: "",
    };
  },
  methods: {
    myIscrollRefresh() {
      this.$nextTick(()=>{
           this.myscroll.refresh();
      })
    },
    liClick(id){
        this.$parent.getSongInfo(id)
    }
  },
  mounted() {
    this.myscroll = new iscroll(this.$refs.wrapper, {
      mouseWheel: true,
      scrollbars: true,
    });
  },
};
</script>

<style>
</style>