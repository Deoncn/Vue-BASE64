<script>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue';
// import HelloWorld from './components/HelloWorld.vue'

// // Define the string
// var decodedStringBtoA = 'Hello World!';

// // Encode the String
// var encodedStringBtoA = btoa(decodedStringBtoA);

// console.log(encodedStringBtoA);


// // Define the string
// var encodedStringAtoB = 'SGVsbG8gV29ybGQh';

// // Decode the String
// var decodedStringAtoB = atob(encodedStringAtoB);

// console.log(decodedStringAtoB);

export default {
  data() {
    return {
      count: "1",
      result: "",
    }
  },
  methods: {
    encode_str_to_base64() {
      var base = this.count;
      this.result = btoa(base)

      console.log(this.result)
    },
    encode_base64_to_str() {
      var base = this.count;
      this.result = atob(base)

      console.log(this.result)
    }


  }

}
</script>

<template>
     <h1>Base64</h1>
  <div >
    <div>
   
    </div>
    <div>
      <input style="width: 800px; height: 45px;" v-model="count">
    </div>
    <div>
      <button style="width: 60px;height: 30px;" @click="encode_str_to_base64()">编码</button>
      <button style="width: 60px;height: 30px;" @click="encode_base64_to_str()">解码</button>
  
    </div>
    <div>
      <input style="width: 800px; height: 45px;" v-model="result">
    </div>

  </div>
</template>

<style>

html{

  max-width: 900px;
}



</style>