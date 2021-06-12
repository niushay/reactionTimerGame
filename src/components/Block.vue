<template>
  <div class="block" v-if="showblock">
      Click Me
  </div>
</template>

<script>
export default {
    props: ['delay'],
    data() {
        return {
            showblock: false
        }
    },
    mounted() {
       console.log("component is mounted")
        setTimeout(() => {
            this.showblock = true
            console.log(this.showblock)
        }, this.delay)
    },
    updated() {
        console.log("Updated!")
    },
    unmounted() {
        console.log("unmounted!")
    },
}
</script>

<style>
    .block{
        width:400px;
        border-radius: 20px;
        background: #0faf87;
        color: white;
        text-align: center;
        padding: 100px 0;
        margin: 40px auto
    }
</style>