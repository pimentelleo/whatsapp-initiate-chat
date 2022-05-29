<template>
  <div>
    <footer class="footer">
      <p>Footer text</p>
      <p>Footer Icon</p>
    </footer>

    <style>
      .footer {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        gap: 4px;
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
  name: 'Footer',
  methods: {
    openWhatsappChat(number) {
      const url = 'https://wa.me/55' + number
      window.open(url, '_blank').focus()
    },
  },
}
</script>
