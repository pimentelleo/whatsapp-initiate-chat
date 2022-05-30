<template>
  <div class="layout">
    <Header class="header" />
    <Nuxt class="content" />

    <Footer />
  </div>
</template>
<style>
.layout {
  display: flex;
  flex-direction: column;
}
.header {
  margin: 10px 16px;
  position: fixed;
  width: 90%;
  height: 6%;
}

.content {
  padding: 16px;
}

.header + .content {
  padding-top: 102px;
}
</style>

<script>
export default {
  data() {
    return {
      mobileNumber: '',
    }
  },
  name: 'Layout',
  methods: {
    changeView(viewPage) {
      return `<${viewPage}>`
    },
  },
}
</script>
