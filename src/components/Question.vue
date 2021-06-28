<template>
  <div class="flex flex-col items-center">
    <span class="mb-2">{{label}}</span>
    <div class="flex">
      <Button @click="onClick(index)" v-for="(answer, index) in answers">{{answer.label}}</Button>
    </div>
  </div>
</template>

<script>
import Button from "./Button.vue";
export default {
  components: {Button},
  props : ['answers', 'label'],
  data : () => ({

  }),
  mounted() {
  },
  methods : {
    onClick(index) {
      this.$emit('answer',index);
    }
  }
}
</script>