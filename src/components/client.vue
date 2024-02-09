<template>
  <div class="client-client" v-bind:class="rootClassName">
    <span class="client-text">{{ quote }}</span>
    <div class="client-author">
      <img alt="image" :src="avatar" class="client-avatar" />
      <div class="client-details">
        <span class="client-text1">{{ author }}</span>
        <span class="client-text2">{{ mention }}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Client',
  props: {
    mention: {
      type: String,
      default: '@agncy',
    },
    quote: {
      type: String,
      default:
        '“Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.“',
    },
    rootClassName: String,
    avatar: {
      type: String,
      default:
        'https://images.unsplash.com/photo-1618151313441-bc79b11e5090?ixid=Mnw5MTMyMXwwfDF8c2VhcmNofDEzfHxwb3RyYWl0fGVufDB8fHx8MTY2OTA2MTI0MQ&ixlib=rb-4.0.3&w=200',
    },
    author: {
      type: String,
      default: 'Joanna Smith',
    },
  },
}
</script>

<style scoped>
.client-client {
  gap: var(--dl-space-space-threeunits);
  width: 450px;
  display: flex;
  position: relative;
  border-color: #ffffff;
  flex-direction: column;
  padding-bottom: var(--dl-space-space-fiveunits);
  border-bottom-width: 1px;
}
.client-text {
  color: #ffffff;
  font-size: 22px;
  line-height: 36px;
}
.client-author {
  gap: var(--dl-space-space-oneandhalfunits);
  display: flex;
  position: relative;
  align-items: center;
  flex-direction: row;
}
.client-avatar {
  width: 60px;
  height: 60px;
  object-fit: cover;
  border-radius: var(--dl-radius-radius-round);
}
.client-details {
  gap: var(--dl-space-space-unit);
  display: flex;
  align-items: center;
  flex-direction: row;
}
.client-text1 {
  color: rgb(255, 255, 255);
  font-size: 20px;
  font-style: normal;
  font-weight: 500;
  line-height: 30px;
}
.client-text2 {
  color: rgb(255, 255, 255);
  font-size: 20px;
  line-height: 30px;
}


@media(max-width: 991px) {
  .client-client {
    gap: var(--dl-space-space-unit);
    width: 100%;
    padding-bottom: var(--dl-space-space-oneandhalfunits);
  }
  .client-text {
    font-size: 16px;
    line-height: 24px;
  }
  .client-author {
    gap: var(--dl-space-space-unit);
  }
  .client-avatar {
    width: 40px;
    height: 40px;
  }
  .client-text1 {
    font-size: 16px;
    line-height: 24px;
  }
  .client-text2 {
    font-size: 16px;
    line-height: 24px;
  }
  .client-root-class-name {
    width: 100%;
  }
}
@media(max-width: 767px) {
  .client-root-class-name1 {
    width: 100%;
  }
}
</style>
