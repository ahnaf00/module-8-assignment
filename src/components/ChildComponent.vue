<script setup>
    import { defineProps, defineEmits } from 'vue';

    const props = defineProps({
    message: String,
    });

    const emit = defineEmits();

    const emitMessage = () => {
        const customMessage = 'Custom message from ChildComponent';
        emit('messageEmitted', customMessage);
    };
</script>
<template>
    <div>
      <p>Received from ParentComponent: {{ message }}</p>
      <button @click="emitMessage">Emit Message</button>
    </div>
</template>
  
  