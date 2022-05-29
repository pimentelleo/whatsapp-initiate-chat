<template>
  <div>Aqui Header</div>
</template>

<script>
export default {
  data() {
    return {
      mobileNumber: '',
    }
  },
  name: 'Layout',
  methods: {
    openWhatsappChat(number) {
      const url = 'https://wa.me/55' + number
      window.open(url, '_blank').focus()
    },
  },
}
</script>
