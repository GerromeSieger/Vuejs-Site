<template>
  <div class="author-author" v-bind:class="rootClassName">
    <img alt="image" :src="avatar" class="author-avatar" />
    <div class="author-details">
      <span class="author-text">{{ author }}</span>
      <span class="author-text1">{{ mention }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Author',
  props: {
    rootClassName: String,
    mention: {
      type: String,
      default: '@spyrl',
    },
    author: {
      type: String,
      default: 'Joanna Smith',
    },
    avatar: {
      type: String,
      default:
        'https://images.unsplash.com/photo-1618151313441-bc79b11e5090?ixid=Mnw5MTMyMXwwfDF8c2VhcmNofDEzfHxwb3RyYWl0fGVufDB8fHx8MTY2OTA2MTI0MQ&ixlib=rb-4.0.3&w=200',
    },
  },
}
</script>

<style scoped>
.author-author {
  gap: var(--dl-space-space-oneandhalfunits);
  display: flex;
  position: relative;
  align-items: center;
  flex-direction: row;
}
.author-avatar {
  width: 60px;
  height: 60px;
  object-fit: cover;
  border-radius: var(--dl-radius-radius-round);
}
.author-details {
  gap: var(--dl-space-space-unit);
  display: flex;
  align-items: center;
  flex-direction: row;
}
.author-text {
  color: rgb(255, 255, 255);
  font-size: 20px;
  font-style: normal;
  font-weight: 500;
  line-height: 30px;
}
.author-text1 {
  color: rgb(255, 255, 255);
  font-size: 20px;
  line-height: 30px;
}
@media(max-width: 991px) {
  .author-author {
    gap: var(--dl-space-space-unit);
  }
  .author-avatar {
    width: 40px;
    height: 40px;
  }
  .author-text {
    font-size: 16px;
    line-height: 24px;
  }
  .author-text1 {
    font-size: 16px;
    line-height: 24px;
  }
}
</style>
