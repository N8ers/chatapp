<template>
  <div>
    <h1>I am chat</h1>

    <div>
      <button @click="selectedUser = 'Joe'">Joe</button>
      <button @click="selectedUser = 'Goon'">Goon</button>
      <button @click="selectedUser = 'Tsuki'">Tsuki</button>
    </div>

    <br/>

    <div v-for="message in messages" :key="message">
      <div>{{ message.user }}: {{ message.message }}</div>
    </div>

    <br />

    <input type="text" placeholder="..." />
    <button>
      send<span v-if="selectedUser"> as {{ selectedUser }}</span>
    </button>
  </div>
</template>

<script>
export default {
  name: 'Chat',
  data() {
    return {
      selectedUser: null,
      messages: [
        { user: 'Joe', message: 'hey' },
        { user: 'Tsuki', message: 'Meow' },
        { user: 'Joe', message: 'Hi cat' },
        { user: 'Goon', message: 'Oh, Tsuki!' },
        { user: 'Tsuki', message: 'Mweooooow' },
      ],
    };
  },
};
</script>
