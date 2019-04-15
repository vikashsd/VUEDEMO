<template>
<div id="container">
<v-header></v-header>
<img :src="image"/>
</div>
</template>

<script>
import header from './header'
export default {
    name:'container',
     components:{       
       'v-header':header
     },
  data() {
    return {
          image:require('assets/1.png'),
    }
  }
}
</script>