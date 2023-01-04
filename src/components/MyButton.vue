<script lang="ts">
import { defineComponent } from "vue-ts-utils";
import type { ButtonProps } from "element-plus";
import { ElButton } from "element-plus";
export default defineComponent(
  {
    inheritAttrs: false,
    created() {
      console.log(this.$attrs);
    },
  },
  { attrs: {} as Partial<ButtonProps> }
);
</script>

<template>
  <div class="btn-wrapper">
    hello
    <ElButton class="btn" v-bind="$attrs"><slot></slot></ElButton>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
