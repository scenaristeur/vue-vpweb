<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png"> -->
    <!-- <FileIcon onChange="fileChanged" color="red"/> -->
    Load a table
    <input ref="input" @change="fileChanged" type="file" id="input">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
// import FileIcon from '@/components/layout/FileIcon.vue'

export default {
  name: 'Home',
  components: {
    // HelloWorld
    // FileIcon
  },
  created () {
    // const fileInput = document.getElementById('input')
    // fileInput.onchange = () => {
    //   this.selectedFile = fileInput.files[0]
    //   console.log(this.selectedFile)
    // }
  },
  watch: {
    selectedFile () {
      console.log(this.selectedFile)
    }
  },
  methods: {
    fileChanged () {
      this.selectedFile = this.$refs.input.files[0]

      console.log(this.selectedFile)
    }
  }
}
</script>
