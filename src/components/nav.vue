<template>
<div style="height:500px">
    <header id="myCarousel" class="carousel slide">
        <!-- Indicators -->
        <ol class="carousel-indicators">
            <li data-target="#myCarousel" data-slide-to="0" class="active" click="slidebar(1)">
    			<div class="fill" id="item1"></div>
            </li>
            <li data-target="#myCarousel" data-slide-to="1" click="slidebar(2)">
            	<div class="fill" id="item2" ></div>
            </li>
            <li data-target="#myCarousel" data-slide-to="2" click="slidebar(3)">
            	<div class="fill" id="item3" ></div>
            </li>
        </ol>

        <!-- Wrapper for Slides -->
        <div class="carousel-inner">
            <div class="item active">
                <div class="fill" id="image1"><div class="top-left">List Your Property</div><div class="centered">Hotel</div></div>
            </div>
            <div class="item">
                <div class="fill" id="image2"><div class="top-left">List Your Property</div><div class="centered">Villa</div></div>
            </div>
            <div class="item">
                <div class="fill" id="image3"><div class="top-left">List Your Property</div><div class="centered">Apartments</div></div>
            </div>
        </div>

    </header>
    </div>
</template>

<script>
   export default {
     name: 'nav',
     methods: {
      slidebar (c) {
        if(!c){
           c = 2 
        }
        let id
      setInterval(function(){
        id = 'image' + c
        let d = c-1 
        let id1 = c==1 ? 'image3':'image' + d
        document.getElementById(id1).parentElement.classList.remove("active")
        document.getElementById(id).parentElement.classList.add("active") 
        if(c==3){c=1} else{ c++} }, 3000 ) 
       } 
            
     },
     mounted (){
       this.slidebar()
   }
   }
</script>
 
<style>
.centered {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    font-size:35px;
    color:white;
}
.top-left {
    position: absolute;
    top: 10%;
    left: 42%;
    font-size:30px;
    color:white;
}
    ol.carousel-indicators li{
    width: 100px;
    height: 100px;
    border-color: transparent;
}

ol.carousel-indicators li.active{
    width: 100px;
    height: 100px;
    border-color: transparent;
    background-color: transparent;
}

ol.carousel-indicators li div{
    border-radius: 50%;
    background: rgba(0,0,0,0.8);
}

ol.carousel-indicators li.active div{
    border-radius: 50%;
    background: rgba(255,255,255,0.8);
}

.carousel,
.item,
.active {
    height: 100%;
}

.carousel-inner {
    height: 100%;
}

.fill {
    width: 100%;
    height: 100%;
    background-position: center;
    -webkit-background-size: cover;
    -moz-background-size: cover;
    background-size: cover;
    -o-background-size: cover;
}

#image1 {
    background-image:url('../assets/hotel.jpg');
}

#image2 {
    background-image:url('../assets/villa.jpg');
}

#image3 {
    background-image:url('../assets/apartment.jpg');
}

#item1 {
    background-image:url('http://vira1368.persiangig.com/bootstrap%20template/full-slider/images/hover-pag-1.png');
}

#item2 {
    background-image:url('http://vira1368.persiangig.com/bootstrap%20template/full-slider/images/hover-pag-2.png');
}

#item3 {
    background-image:url('http://vira1368.persiangig.com/bootstrap%20template/full-slider/images/hover-pag-3.png');
}
</style>