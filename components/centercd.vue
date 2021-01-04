<template>
   <div class="player_con">
          <img src="../assets/images/player_bar.png" :class="{play_bar:true,playing:playing}" />
          <!-- 黑胶碟片 -->
          <img src="../assets/images/disc.png" :class="{disc:true,autoRotate:true,playing:playing}" />
          <img :src="picurl" :class="{cover:true,autoRotate:true,playing:playing}" />
        </div>
</template>

<script>
export default {
    data() {
        return {
            playing:false,
            picurl:'https://ss1.bdstatic.com/70cFuXSh_Q1YnxGkpoWK1HF6hhy/it/u=1089874897,1268118658&fm=26&gp=0.jpg',
        }
    },
}
</script>

<style>

</style>