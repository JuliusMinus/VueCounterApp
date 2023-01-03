

<script setup>

// composition api


import { ref } from "vue"
const count = ref(10);

const addToCount = () => {

  console.log("hello from add to count")
  count.value = count.value + 1

}

const subtractFromCount = () => {
  console.log("hello from subtract to count")
  count.value = count.value - 1
}

</script>


<!-- <script>


// option api


export default (

  {

    data() {
      return {
        count: 0
      }
    },
    methods: {
      addToCount() {
        this.count = this.count + 1
      },
      subtractFromCount() {
        this.count = this.count - 1
      }
    }


  }

)

</script> -->




<template>
  <main>
    <div>
      <h4>
        The current count is...
      </h4>
      <h1>{{ count }}</h1>
      <button @click="subtractFromCount()">-</button>
      <button @click="addToCount()">+</button>

    </div>
  </main>
</template>

<style scoped>
main {

  background-color: brown;
  height: 100vh;
  width: 100vw;
  display: flex;
  align-items: center;
  justify-content: center;



}

div {

  text-align: center;
}
</style>

