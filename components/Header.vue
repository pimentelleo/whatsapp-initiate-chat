<template>
  <div>
    <footer class="header">
      <div class="pedido-button">
        <el-button type="success" @click="changeView(AppTest2)" round
          >Render2</el-button
        >
        <el-button type="success" @click="changeView(AppTest)" round
          >Render1</el-button
        >
        <NuxtLink to="/AppTest">Home page</NuxtLink>
      </div>
    </footer>

    <style>
      .header {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: space-around;
        gap: 4px;
        z-index: 2 !important;
        background-color: black;

        .text {
          color: white;
        }
        top: 0;
      }
      .pedido-button {
        background-color: blue;
        justify-content: space-between;
        height: 40px;
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
  name: 'Layout',
  methods: {
    changeView(viewPage) {
      return `<${viewPage}>`
    },
  },
}
</script>
