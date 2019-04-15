<template>
  <div id="listing" class="container" style="float:right">
          <div class=" well1  col-md-10">
            <div class="row">
                      <div class="col-md-9" v-for="item in ListColl">
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
name: 'list',
 props: {
   ListColl: {
  title: String,
  likes: Number,
  isPublished: Boolean,
  commentIds: Array,
  author: Object}
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

