<template>
  <div>
    <h2>Cek Status Pendaftaran</h2>
    <form @submit.prevent="checkStatus">
      <label for="email">Email:</label>
      <input type="email" v-model="email" required />

      <button type="submit">Cek Status</button>
    </form>
    <div v-if="status !== null">
      <p>Status Pendaftaran: {{ status }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      email: "",
      status: null,
    };
  },
  methods: {
    checkStatus() {
      this.status = Math.random() < 0.5 ? "Diterima" : "Ditolak";
    },
  },
};
</script>
