<template>
  <div>
    <el-input
      placeholder="Insira o numero no whatsapp com DDD"
      v-model="mobileNumber"
      type="number"
      pattern="[0-9]*"
      inputmode="numeric"
    ></el-input>
    <p>{{ mobileNumber }}</p>

    <el-button type="primary" @click="openWhatsappChat(mobileNumber)"
      >Abrir conversa</el-button
    >
  </div>
</template>

<script>
export default {
  data() {
    return {
      mobileNumber: '',
    }
  },
  name: 'AppTest',
  methods: {
    openWhatsappChat(number) {
      const url = 'https://wa.me/55' + number
      window.open(url, '_blank').focus()
    },
  },
}
</script>
