<template>
  <div>
    <h3>Conversation</h3>
    <h1>{{ conversation }}</h1>

    <br/>

    <!-- <div v-for="message in messages" :key="message">
      <div>{{ message.user }}: {{ message.message }}</div>
      <div>{{ message.timestamp }}</div>
    </div> -->

    <br />

    <input type="text" placeholder="..." />
    <button>send</button>
  </div>
</template>

<script>
export default {
  name: 'Conversation',
  props: {
    conversation: {
      type: Object,
      required: false,
      default: () => {},
    },
  },
  data() {
    return {
    };
  },
};
</script>
