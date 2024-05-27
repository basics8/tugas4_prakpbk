<!-- ParentComponent.vue -->
<template>
  <div>
    <h1>Data di ParentComponent</h1>
    <p v-if="dataFromChild">{{ dataFromChild }}</p>
    <ChildComponent1 @child-event="handleChildEvent" />
    <ChildComponent2 @button-click="handleButtonClick" />
  </div>
</template>

<script>
import ChildComponent1 from './ChildComponent1.vue';
import ChildComponent2 from './ChildComponent2.vue';

export default {
  components: {
    ChildComponent1,
    ChildComponent2
  },
  data() {
    return {
      dataFromChild: ''
    };
  },
  methods: {
    handleChildEvent(data) {
      this.dataFromChild = data;
    },
    handleButtonClick(data) {
      this.dataFromChild = data;
    }
  }
};
</script>
