<template>
  <div>
    <AppTest /><AppTest /><AppTest /><AppTest /><AppTest /><AppTest /><AppTest /><AppTest /><AppTest /><AppTest /><AppTest /><AppTest /><AppTest /><AppTest /><AppTest /><AppTest /><AppTest /><AppTest /><AppTest /><AppTest /><AppTest /><AppTest /><AppTest /><AppTest /><AppTest /><AppTest />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'IndexPage',

  methods: {
    changeView(viewPage) {
      return `<${viewPage}>`
    },
  },
})
</script>
