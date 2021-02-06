<template>
  <div>
    <h1>I am chat</h1>
    <Rooms :conversations="conversations" @selectConversation="selectConversation" />
    <Conversation v-if="selectedConversation" :selectedConversation="selectedConversation" />
  </div>
</template>

<script>
import Rooms from './Rooms.vue';
import Conversation from './Conversation.vue';

export default {
  name: 'Chat',
  components: {
    Rooms, Conversation,
  },
  data() {
    return {
      selectedConversation: null,
      users: [
        { uid: 3 },
      ],
      messages: [
        {
          id: 10, conversation_id: 3, sender_uid: 3, message: 'Meow', timestamp: '111',
        },
      ],
      conversations: [
        { id: 1, name: 'Joe' },
        { id: 2, name: 'Goon' },
        { id: 3, name: 'Tsuki' },
      ],
    };
  },
  methods: {
    selectConversation(conversation) {
      this.selectedConversation = conversation;
    },
  },
};
</script>
