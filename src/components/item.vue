<template>
  <div class="item-item service">
    <div class="item-details">
      <span class="item-text">{{ title }}</span>
      <span class="item-text1">{{ tags }}</span>
    </div>
    <svg viewBox="0 0 1024 1024" class="item-icon">
      <path
        d="M298.667 341.333h323.669l-353.835 353.835c-16.683 16.683-16.683 43.691 0 60.331s43.691 16.683 60.331 0l353.835-353.835v323.669c0 23.552 19.115 42.667 42.667 42.667s42.667-19.115 42.667-42.667v-426.667c0-5.803-1.152-11.307-3.243-16.341s-5.163-9.728-9.216-13.781c-0.043-0.043-0.043-0.043-0.085-0.085-3.925-3.925-8.619-7.083-13.781-9.216-5.035-2.091-10.539-3.243-16.341-3.243h-426.667c-23.552 0-42.667 19.115-42.667 42.667s19.115 42.667 42.667 42.667z"
      ></path>
    </svg>
  </div>
</template>

<script>
export default {
  name: 'Item',
  props: {
    title: {
      type: String,
      default: 'Eiusmod',
    },
    tags: {
      type: String,
      default: 'Strategy / Webdevelopment / Marketing',
    },
  },
}
</script>

<style scoped>
.item-item {
  position: relative;
}
.item-details {
  gap: var(--dl-space-space-oneandhalfunits);
  display: flex;
  align-items: center;
  flex-direction: row;
  justify-content: flex-start;
}
.item-text {
  color: #ffffff;
  width: 190px;
  font-size: 24px;
  font-style: normal;
  font-weight: 500;
  line-height: 36px;
}
.item-text1 {
  color: rgb(153, 153, 153);
  font-size: 24px;
  line-height: 36px;
}
.item-icon {
  fill: #ffffff;
  width: 30px;
  height: 30px;
}
@media(max-width: 991px) {
  .item-item {
    width: 100%;
    align-items: flex-start;
    padding-top: var(--dl-space-space-unit);
    flex-direction: row;
    padding-bottom: var(--dl-space-space-unit);
    justify-content: space-between;
  }
  .item-details {
    gap: var(--dl-space-space-halfunit);
    align-items: flex-start;
    flex-direction: column;
  }
  .item-text {
    font-size: 16px;
    line-height: 24px;
  }
  .item-text1 {
    font-size: 14px;
    line-height: 21px;
  }
  .item-icon {
    width: 12px;
    height: 12px;
  }
}
</style>
