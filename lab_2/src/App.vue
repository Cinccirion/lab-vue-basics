<template>
  <div>
 <Navbar class='navigation' />
 <div class='orange'> {{Suma}} </div>
 <div id='word' v-for="word in words" :key="word.id"> {{ word }} </div>
 <button @click="botoncico">Log In</button>
  <button @click='Color' v-for="Color in words" :key='Color'>Color</button>
<Card class='Card' />





    <router-view/>
  </div>

</template>

<script>
import Navbar from "./components/Navbar.vue";
import Footer from "./components/Footer.vue";


export default {
  
  
  components: {
    Navbar,
    Footer,
    Card,
    Button,
    
  },
  data () {
    return {
      Suma: '2+2',
     words: ['agua','luz','petarda'],
      botoncico: true,
    };
    
  },
  methods: {
    Suma () {
      return '2+2';
    },
    botoncico () {
      if (this.orange === "orange") {
        this.orange = "red";
      } else {
        this.orange = "orange;"
      }
    }
  }
  }
</script>

<style>

.navigation {
  justify-content: center;
  align-content: center;
}
.orange {
  color: orange;
}
.red {
  color: red;
}

</style>
