<template>
  <el-container>
    <div
        :class="className"
        :style="{
          background: 'url(' + imgSrc + ') no-repeat',
          backgroundPosition: 'center',
          backgroundSize: '100%'}"
          >
      </div>
  </el-container>
</template>

<script>
export default {
  name: 'CommonBanner',
  props: {
    imgSrc: {
      type: String,
      required: true
    }
  },
  computed: {
    className () {
      return this.$ISMOBILE ? 'image mobile-image' : 'image'
    }
  }
}
</script>

<style scoped>
.image {
  height: 25rem;
  width: 100%;
}
.image.mobile-image {
  height: 15rem;
}
</style>
