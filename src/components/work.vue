<template>
  <div class="work-work">
    <img alt="image" :src="image" class="work-image" />
    <div class="work-details">
      <div class="work-header">
        <div class="work-heading">
          <span class="work-text">{{ title }}</span>
          <app-link></app-link>
        </div>
        <span class="work-text1">{{ description }}</span>
      </div>
      <div class="work-tags">
        <app-tag></app-tag>
        <app-tag tag="Strategy"></app-tag>
        <app-tag tag="Web Development"></app-tag>
      </div>
    </div>
  </div>
</template>

<script>
import AppLink from './link'
import AppTag from './tag'

export default {
  name: 'Work',
  props: {
    image: {
      type: String,
      default: '/work%20%231-1500w.png',
    },
    description: {
      type: String,
      default:
        'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt.',
    },
    title: {
      type: String,
      default: 'MOTECH',
    },
  },
  components: {
    AppLink,
    AppTag,
  },
}
</script>

<style scoped>
.work-work {
  gap: 140px;
  width: 100%;
  display: flex;
  position: relative;
  align-items: flex-start;
  padding-top: var(--dl-space-space-twounits);
  border-color: #151515;
  padding-left: var(--dl-space-space-fiveunits);
  flex-direction: row;
  padding-bottom: var(--dl-space-space-twounits);
  border-bottom-width: 1px;
}
.work-image {
  width: 417px;
  height: 520px;
  object-fit: cover;
}
.work-details {
  flex: 1;
  height: 520px;
  display: flex;
  align-items: flex-start;
  padding-top: var(--dl-space-space-threeunits);
  flex-direction: column;
  padding-bottom: var(--dl-space-space-threeunits);
  justify-content: space-between;
}
.work-header {
  gap: var(--dl-space-space-threeunits);
  width: 100%;
  display: flex;
  align-items: flex-start;
  flex-direction: column;
}
.work-heading {
  width: 100%;
  display: flex;
  align-items: flex-start;
  flex-direction: row;
  justify-content: space-between;
}
.work-text {
  color: rgb(21, 21, 21);
  font-size: 40px;
  font-style: normal;
  font-weight: 500;
  line-height: 36px;
  text-transform: uppercase;
}
.work-text1 {
  color: rgb(21, 21, 21);
  font-size: 24px;
  line-height: 36px;
}
.work-tags {
  gap: var(--dl-space-space-halfunit);
  display: flex;
  flex-wrap: wrap;
  align-items: flex-start;
  flex-direction: row;
}
@media(max-width: 991px) {
  .work-work {
    gap: 0px;
    padding-top: var(--dl-space-space-threeunits);
    padding-left: 0;
    padding-right: 0;
    flex-direction: column;
    padding-bottom: var(--dl-space-space-threeunits);
  }
  .work-image {
    width: 100%;
  }
  .work-details {
    gap: var(--dl-space-space-oneandhalfunits);
    align-items: flex-start;
    padding-top: var(--dl-space-space-oneandhalfunits);
    padding-bottom: 0px;
    justify-content: flex-start;
  }
  .work-header {
    gap: var(--dl-space-space-unit);
  }
  .work-heading {
    align-items: center;
  }
  .work-text {
    font-size: 24px;
    line-height: 21px;
  }
  .work-text1 {
    font-size: 16px;
    line-height: 24px;
  }
}
</style>
