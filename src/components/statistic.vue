<template>
  <div class="statistic-statistic" v-bind:class="rootClassName">
    <span class="statistic-sta">{{ caption }}</span>
    <span class="statistic-sta1">{{ value }}</span>
  </div>
</template>

<script>
export default {
  name: 'Statistic',
  props: {
    rootClassName: String,
    value: {
      type: String,
      default: '12',
    },
    caption: {
      type: String,
      default: 'Years of growth',
    },
  },
}
</script>

<style scoped>
.statistic-statistic {
  gap: var(--dl-space-space-threeunits);
  width: 346px;
  display: flex;
  position: relative;
  align-items: flex-start;
  border-color: #ffffff;
  flex-direction: column;
  padding-bottom: var(--dl-space-space-fiveunits);
  border-bottom-width: 1px;
}
.statistic-sta {
  color: rgb(153, 153, 153);
  font-size: 20px;
  line-height: 30px;
  letter-spacing: 3%;
  text-transform: uppercase;
}
.statistic-sta1 {
  color: rgb(255, 255, 255);
  font-size: 80px;
  font-style: normal;
  font-weight: 500;
  line-height: 72px;
}






@media(max-width: 991px) {
  .statistic-statistic {
    gap: var(--dl-space-space-unit);
    padding-bottom: var(--dl-space-space-oneandhalfunits);
  }
  .statistic-sta {
    font-size: 11px;
    line-height: 16.5px;
  }
  .statistic-sta1 {
    font-size: 40px;
    line-height: 36px;
  }
  .statistic-root-class-name {
    width: 100%;
  }
  .statistic-root-class-name1 {
    width: 100%;
  }
  .statistic-root-class-name2 {
    width: 100%;
  }
  .statistic-root-class-name3 {
    width: 100%;
  }
  .statistic-root-class-name4 {
    width: 100%;
  }
  .statistic-root-class-name5 {
    width: 100%;
  }
}
</style>
