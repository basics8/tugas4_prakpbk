<!-- ChildComponent1.vue -->
<template>
  <div>
    <h2>ChildComponent1</h2>
    <button @click="sendDataToParent">Kirim Data ke Parent</button>
  </div>
</template>

<script>
export default {
  methods: {
    sendDataToParent() {
      this.$emit('child-event', 'Data dari ChildComponent1');
    }
  }
};
</script>
