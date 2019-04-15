<template>
  <div id="listing" class="container">
        <div class=" well1  col-md-6 well" style="background-color: white">
            <div class="row">
                <div class="col-md-9">
                    <div class="row"> 
                    <div style="margin:30px">{{ListText}}</div>
                      <div class="col-md-3" v-for="item in List">
                      <router-link v-bind:to="'/image'"><img class="grow" :src="item"/></router-link>
                      </div>                     
                    </div>                   
                  </div>
                </div>
          </div>
        <div v-if="ListColl.length" class=" well1  col-md-5 well" style="margin:20px">
             <p align="center">Your Listing</p>
             <div class="row">
                      <div class="col-md-12" v-for="item in ListColl">
                          <div class="example">
                          <p>{{item}}</p>
                       </div>
                      </div>                                    
                </div>
          </div>
    </div>
</template>
<script>
export default {
name: 'listing',
 props: {
   List: { },
   ListText:{
     type:String
   },
   ListColl: {
    title: String,
    likes: Number,
    isPublished: Boolean,
    commentIds: Array,
    author: Object 
  }
 }
}
</script>
<style>
.example {
    border: 1px solid;
    padding: 10px;
    box-shadow: 5px 10px #888888;
    margin:10px
}
</style>


