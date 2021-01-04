<template>
  <div class="comment_list" ref="comment_list">
    <div>
      <dl v-for="(item, index) in commments" :key="index">
        <dt>
          <img :src="item.user.avatarUrl" alt="" />
        </dt>
        <dd class="name">{{ item.user.nickname }}</dd>
        <dd class="detail">
          {{item.content}}
        </dd>
      </dl>
    </div>
  </div>
</template>

<script>
import iscroll from "iscroll";
export default {
  data() {
    return {
      commments: "",
    };
  },
  methods: {
    getmyscroll() {
      this.$nextTick(()=>{
           this.myscroll.refresh();
      })
    },
  },
  mounted() {
    this.myscroll = new iscroll(this.$refs.comment_list, {
      mouseWheel: true,
      scrollbars: true,
    });
  },
};
</script>

<style>
</style>