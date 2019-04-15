<template>
<div id="home">

<v-header></v-header>
<v-nav></v-nav>

   <!--<div class="row">
      <div class=" well1  col-md-12">
         <div class=" well1  col-md-10">
            <h4>Let's Configure Your Listing</h4>
         </div>
         <div class=" well1  col-md-2">
            <img :src="image6" />
         </div> 
          <div class=" well1  col-md-2">
         </div>
      </div>
   </div>-->
    <!-- <v-clist :ListColl="ListColl"></v-clist>-->
    <v-Listing :List="FirstList" :ListColl="ListColl" :ListText="FirstListText"></v-Listing>
   <div class="row">
      <div class="col-md-1">
          Select option
      </div>
      <div class="col-md-9">
         <div class="col-md-3">
            <select class="form-control mrg-btm-18">
               <option>Other Select</option>
               <option>B&B</option>
               <option>Villa</option>
               <option>Apartment</option>
               <option>Resort</option>
            </select>
         </div>
         <div class="col-md-8"> 
         </div>
      </div>
      <div class="col-md-1"></div>
   </div>
   <v-Listing :List="SecondList" :ListColl="[]" :ListText="SecondListText"></v-Listing>
   <div class="well1  row">
      <div class="col-md-3"></div>
      <div class="col-md-3">
         <input type="button" value="ADD" class="backBtn btn" @click="addList()">
      </div>
   </div>
   <v-navigater></v-navigater>
   <v-footer></v-footer>
   
</div>
</template>
<script>
   import listing from './Listing'
   import header from './header'
   import navigater from './navigater'
   import footer from './footer'
   import nav from './nav'
   import clist from './list'
   export default {
     name: 'home',
     components:{
       'v-Listing':listing,
       'v-header':header,
       'v-navigater':navigater,
       'v-footer':footer, 
       'v-nav':nav,
       'v-clist': clist
     },
    data() {
       return {
         image7:require('assets/topMeu.png'),
         image6:require('assets/Capture.png'),
         FirstList:[require('assets/5.png'),require('assets/4.png'),require('assets/3.png'),require('assets/2.png')],
         FirstListText:"CHOOSE YOUR ACCOMODATION",
         SecondList:[require('assets/1.png'),require('assets/4.png')],
         SecondListText:"Room Type",
         ListColl: [],
         count : 1
       }
     },
    methods:{
      addList() {
          let id = 'Room'  + this.count ++ 
         this.ListColl.push(id)
      }
        
    }
   }
</script>