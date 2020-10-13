<template>
  <Layout class-prefix="layout">
    <Tags :data-source="tags"/>
    <Notes/>
    <Types/>
    <NumberPad/>
  </Layout>
</template>

<script lang="js">

import NumberPad from "@/components/Money/NumberPad.vue";
import Types from "@/components/Money/Types.vue";
import Tags from "@/components/Money/Tags.vue";
import Notes from "@/components/Money/Notes.vue";

export default {
  name: "Money",
  components: {Notes, Tags, Types, NumberPad},
  data(){
    return{
      tags:['衣','食','住','行']
    }
  }
}
</script>

<style scoped lang="scss">
@import "~@/assets/style/helper.scss";
</style>