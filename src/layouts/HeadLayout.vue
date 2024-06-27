<template>
  <div></div>
</template>

<script>
export default {
  name: "HeadLayout",
  props: {
    title: {
      type: String,
      required: true,
    },
    desc: {
      type: String,
      required: true,
    },
    keywords: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped></style>
