<!-- ChildComponent2.vue -->
<template>
    <div>
      <h2>ChildComponent2</h2>
      <button @click="sendDataToParent">Kirim Data ke Parent</button>
    </div>
  </template>
  
  <script>
  export default {
    methods: {
      sendDataToParent() {
        this.$emit('button-click', 'Data dari ChildComponent2');
      }
    }
  };
  </script>
  