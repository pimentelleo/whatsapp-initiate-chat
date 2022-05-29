<template>
  <div>
    <Header />
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
    <style>
      .el-row {
        margin-bottom: 20px;
        &:last-child {
          margin-bottom: 0;
        }
      }
      .el-col {
        border-radius: 4px;
      }
      .bg-purple-dark {
        background: #99a9bf;
      }
      .bg-purple {
        background: #d3dce6;
      }
      .bg-purple-light {
        background: #e5e9f2;
      }
      .grid-content {
        border-radius: 4px;
        min-height: 36px;
      }
      .row-bg {
        padding: 10px 0;
        background-color: #f9fafc;
      }
    </style>
  </div>
</template>

<script>
export default {
  data() {
    return {
      mobileNumber: '',
    }
  },
  name: 'Qualquercoisa',
  methods: {
    openWhatsappChat(number) {
      const url = 'https://wa.me/55' + number
      window.open(url, '_blank').focus()
    },
  },
}
</script>
