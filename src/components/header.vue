<template>
     <div id="header" class="row">
      <div class=" well1  col-md-12 bgColorBlue" style="height:50px">
         <div class=" well1  col-md-3 bgColorBlue">
            <font size="5" color="white">Demo</font>
         </div>
          <router-link v-bind:to="'/'" class="headerMenu btn"><i class="fa fa-home"></i> Home </router-link>
           <a class="headerMenu btn"><i class="fa fa-search-plus"></i>Login </a>
           <a class="headerMenu btn"><i class="fa fa-sign-in"></i> Sign Up </a>
           <a class="headerMenu btn"><i class="fa fa-building-o"></i>List My Place </a>
           <a class="headerMenu btn"><i class="fa fa-paper-plane"></i> My Travel </a>
           <a class="headerMenu btn"><i class="fa fa-sort-down"></i> EUR </a>
           <a class="headerMenu btn"><i class="fa fa-language"></i> English </a>
           <a class="headerMenu btn"><i class="fa fa-shopping-basket"></i></a>
           <a class="headerMenu btn"><i class="fa fa-heart"></i></a>
           <a class="headerMenu btn"><i class="fa fa-download"></i></a>
         </div>
      </div>
</template>

 
