<template>
  <div class="tag-container"><span class="tag-tag tag">{{ tag }}</span></div>
</template>

<script>
export default {
  name: 'Tag',
  props: {
    tag: {
      type: String,
      default: 'Branding',
    },
  },
}
</script>

<style scoped>
.tag-container {
  display: flex;
  position: relative;
}
.tag-tag {
  transition: 0.3s;
}
.tag-tag:hover {
  color: #fff;
  background-color: #235536;
}
@media(max-width: 991px) {
  .tag-tag {
    font-size: 12px;
    padding-top: 12px;
    white-space: nowrap;
    padding-left: var(--dl-space-space-unit);
    padding-right: var(--dl-space-space-unit);
    padding-bottom: 12px;
  }
}
</style>
