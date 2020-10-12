<template>
  <nav>
    <router-link class="item" active-class="selected" to="/money">
      <Icon name="money"/>
      记账
    </router-link>
    <router-link class="item" active-class="selected" to="/labels">
      <Icon name="labels" />
      标签
    </router-link>
    <router-link class="item" active-class="selected" to="/statistics">
      <Icon name="statistics" />
      统计
    </router-link>
  </Nav>
</template>

<script lang="ts">

import Icon from "@/components/Icon.vue";
export default {
  name: "Nav",
  components: {Icon}
}
</script>

<style scoped lang="scss">
@import "~@/assets/style/helper.scss";
nav{
  @extend %outerShoadow;
  display: flex;
  flex-direction: row;
  font-size: 12px;
  > .item{
    padding: 2px 0;
    width: 33.33%;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    .icon{
      width: 32px;
      height: 32px;
    }
  }
  > .item.selected{
    color: $color-highlight;
  }
}
</style>