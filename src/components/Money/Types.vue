<template>
  <div>
    <ul class="types">
      <li :class="type === '-' && 'selected'" @click="selectType('-')">支出</li>
      <li :class="type === '+' && 'selected'" @click="selectType('+')">收入</li>
    </ul>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import {Component, Prop} from 'vue-property-decorator'; //引入Component装饰器，vue-property-decorator是第三方写的

//好处1 文档自动提示更智能
//好处2 你不能随便写 .toString()
//好处3 编译报错，无法变成js，严谨
@Component //告诉ts，这是vue的组件
export default class Types extends Vue {
  type = '-'; //‘-’表示支出，'+'表示收入

  selectType(type: string) { //string是表示type是字符串类型
    if (type !== '-' && type !== '+') {
      throw new Error('type is unkonw');
    }
    this.type = type;
  }
}

</script>

<style scoped lang="scss">
.types {
  background: #c4c4c4;
  display: flex;
  text-align: center;
  font-size: 24px;

  > li {
    width: 50%;
    height: 64px;
    display: flex;
    justify-content: center;
    align-items: center;

    &.selected {
      position: relative;

      &::after {
        content: "";
        position: absolute;
        bottom: 0;
        left: 0;
        right: 0;
        height: 4px;
        background: #333;
      }

    }
  }
}
</style>