<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="c-topline">
    <div class="x-container">
      <div class="headline">
        <slot name="headline"></slot>
      </div>
      <div class="content" v-if="$slots.content">
        <slot name="content"></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: 'topline'
}
</script>

<style lang="scss" src="./topline.scss" scoped></style>
