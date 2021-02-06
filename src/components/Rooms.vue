<template>
  <div>

    <h3>conversations:</h3>
    <div v-for="conversation in conversations" :key="conversation">
      <div @click="selectedConversation(conversation)">{{ conversation.name }}</div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'Rooms',
  props: {
    conversations: {
      type: Object,
      reuired: true,
      default: () => {},
    },
  },
  data() {
    return {
      selectedUser: null,
    };
  },
  methods: {
    selectedConversation(conversation) {
      this.$emit('selectConversation', conversation);
    },
  },
};
</script>
