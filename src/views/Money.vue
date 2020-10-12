<template>
  <Layout class-prefix="layout">
    <Tags/>
    <Notes/>
    <types xxx="hi"/>
    <NumberPad/>
  </Layout>
</template>

<script lang="ts">

import NumberPad from "@/components/Money/NumberPad.vue";
import Types from "@/components/Money/Types.vue";
import Tags from "@/components/Money/Tags.vue";
import Notes from "@/components/Money/Notes.vue";

export default {
  name: "Money",
  components: {Notes, Tags, Types, NumberPad},
}
</script>

<style scoped lang="scss">
@import "~@/assets/style/helper.scss";
</style>