<template>
  <div class="small-video card col-md-5 col-xl-3 col-xxl-2">
    <img src="../assets/vido/1/1.png" alt="" class="card-img-top">
    <div class="card-body">
      <span v-if="isTitleTooLong" class="title">{{ truncatedTitle }}</span>
      <span v-else class="title">{{ truncatedTitle }}</span>
      <br>
      <span v-if="isAuthorTooLong" class="author">{{ truncatedAuthor }}</span>
      <span v-else class="author">{{ truncatedAuthor }}</span>
      <br>
      <span class="time">12:34</span>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      originalTitle: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum",
      correctTitleLength: 50,
      originalAuthor: "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum",
      correctAuthorLength: 20,
    };
  },
  computed: {
    isTitleTooLong() {
      return this.originalTitle.length > this.correctTitleLength;
    },
    truncatedTitle() {
      return this.isTitleTooLong ? this.originalTitle.slice(0, this.correctTitleLength) + "..." : this.originalTitle;
    },
    isAuthorTooLong() {
      return this.originalAuthor.length > this.correctAuthorLength;
    },
    truncatedAuthor() {
      return this.isAuthorTooLong ? this.originalAuthor.slice(0, this.correctAuthorLength) + "..." : this.originalAuthor;
    },
  },
};
</script>

<style scoped>

.small-video{
  background-color: red;
  position: relative;
}
/* .small-video .title{

} */
.small-video .author{
  font-size: small;
  position: absolute;
  left: 15px;
  bottom: 8px;
}
.small-video .time{
  position: absolute;
  padding: 0 3px;
  right: 8px;
  top: 8px;
  color: var(--vt-c-purple);
  background-color: hsla(0, 0%, 12%, 0.9);
}

</style>