<template>
  <div>
    <p>Name: {{ userInfo.name }}</p>
    <p>Age: {{ userInfo.age }}</p>

    <button @click="sendData">Send Data To Parent</button>
  </div>
</template>

<script>
export default {
  props: {
    userInfo: Object,
  },
  data() {
    return { dataForParent: "DATA SENT" };
  },
  methods: {
    sendData() {
      this.$emit("childData", this.dataForParent);
    },
  },
};
</script>

<style scoped>
div {
  color: rgb(74, 81, 185);
  font-size: 30px;
}
</style>
