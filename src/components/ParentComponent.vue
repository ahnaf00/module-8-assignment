<script setup>
    import { ref } from 'vue';
    import ChildComponent from './ChildComponent.vue';

    const parentMessage = 'Hello from ParentComponent';
    const receivedMessage = ref('');

    const handleMessageEmitted = (message) => {
        receivedMessage.value = message;
    };
</script>
<template>
    <div>
      <ChildComponent :message="parentMessage" @messageEmitted="handleMessageEmitted" />
      <p>Received from ChildComponent: {{ receivedMessage }}</p>
    </div>
  </template>
  
  