<template>
  <div>
    <el-input
      placeholder="COMPONENTE DE NUMERO 2 TESTE TESTE"
      v-model="mobileNumber"
      type="number"
      pattern="[0-9]*"
      inputmode="numeric"
    ></el-input>
    <p>{{ mobileNumber }}</p>

    <el-button type="primary" @click="openWhatsappChat(mobileNumber)"
      >Abrir ISSO DAQUI EH O 2</el-button
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
  name: 'AppTest2',
  methods: {
    openWhatsappChat(number) {
      const url = 'https://wa.me/+55' + number
      window.open(url, '_blank').focus()
    },
  },
}
</script>
