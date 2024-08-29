<template>
  <view class="content">
    <van-calendar
        :poppable="false"
        :show-confirm="false"
        :readonly="true"
        :style="{'--calendar-height':`${inline?'40px':'340px'}`}"
    />
    <view class="arrow">
      <van-icon name="arrow-up" @click="inline=true" v-if="!inline"/>
      <van-icon name="arrow-down" @click="inline=false" v-else/>
    </view>
  </view>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  data() {
    return {
      inline: false
    }
  },
  onLoad() {

  },
  methods: {}
});
</script>

<style scoped>
.content {
  position: relative;
}

.arrow {
  width: 100%;
  position: absolute;
  bottom: -20px;
  text-align: center;
}
</style>
