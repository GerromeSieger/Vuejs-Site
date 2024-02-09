<template>
  <div class="service-service" v-bind:class="rootClassName">
    <h3 class="service-title">{{ title }}</h3>
    <span class="service-description">{{ description }}</span>
  </div>
</template>

<script>
export default {
  name: 'Service',
  props: {
    title: {
      type: String,
      default: 'Branding',
    },
    rootClassName: String,
    description: {
      type: String,
      default:
        'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.',
    },
  },
}
</script>

<style scoped>
.service-service {
  gap: var(--dl-space-space-twounits);
  width: 100%;
  display: flex;
  position: relative;
  max-width: 350px;
  align-items: flex-start;
  border-color: #151515;
  flex-direction: column;
  padding-bottom: var(--dl-space-space-fourunits);
  border-bottom-width: 1px;
}
.service-title {
  font-size: 40px;
  font-style: normal;
  font-weight: 500;
  line-height: 36px;
  white-space: nowrap;
}
.service-description {
  font-size: 22px;
  line-height: 36px;
}






@media(max-width: 991px) {
  .service-service {
    gap: var(--dl-space-space-unit);
    padding-bottom: var(--dl-space-space-unit);
  }
  .service-title {
    font-size: 18px;
    line-height: 16px;
  }
  .service-description {
    font-size: 14px;
    line-height: 21px;
  }
  .service-root-class-name {
    max-width: 100%;
  }
  .service-root-class-name1 {
    max-width: 100%;
  }
  .service-root-class-name2 {
    max-width: 100%;
  }
  .service-root-class-name3 {
    max-width: 100%;
  }
  .service-root-class-name4 {
    max-width: 100%;
  }
  .service-root-class-name5 {
    max-width: 100%;
  }
}
</style>
