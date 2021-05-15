<template>

<div >
  <!-- The core Firebase JS SDK is always required and must be listed first -->
<script src="/__/firebase/8.6.1/firebase-app.js"></script>

<!-- TODO: Add SDKs for Firebase products that you want to use
     https://firebase.google.com/docs/web/setup#available-libraries -->

<!-- Initialize Firebase -->
<script src="/__/firebase/init.js"></script>
  <div class="top">
   <div class="first p-5">
    <div class="card c1">
  <div class="card-content">
    <div class="content ">
     <p class="one"><b style="color:#ffd65d">Share feelings</b><b style="color:white"> without being judged</b></p><br>
     <b-button class="button" style="border-radius:8px; background-color:#ffd65d ; border:none">Share Feelings</b-button>
    </div>
  </div>
</div></div>
<p class="center p-5" ><b style="color:white">Join . Share . Feel Relif</b></p></div>
<p class="center" style="font-size:25px ; font-weight:400px ; margin:10px ; padding:10px ">A Community to spread positivity</p>
<div class="columns mt-3">
  <div class="column mr-1  third">
<div class="card is-two-fifths wrapper m-5 p-5" v-for="(data,i) in item1" :key="i" style="background-color:#ffd65d">
  <div class="card-content">
    <div class="content ">
     <p><b style="background-color:#fff; border-radius:12px" class="p-3"> {{data.heading}}</b></p><br>
     <p>{{data.content}}</p>
     <b>{{data.user}}</b>
     <p>{{data.time}}</p>
    </div>
  </div>
</div>
<p class="center m-5 p-5" style="color:white"> Share whats on your mind with the community.<br>
<b-button class="button m-5 p-5" style="border-radius:8px; background-color:#ffd65d ; border:none"> Share Feelings</b-button></p>

  </div>

  <div class="column ml-1 third2">
<div class="card m-5 p-5" v-for="(data,i) in item" :key="i" style="background-color:#252525">
  <div class="card-content">
    <div class="content ">
     <p><b style="background-color:#F4f4f4; border-radius:12px" class="p-3"> {{data.heading}}</b></p><br>
     <p  style="color:#fff">{{data.content}}</p>
     <b  style="color:#ffd65d">{{data.user}}</b>
     <p  style="color:#fff">{{data.time}}</p>
    </div>
  </div>
</div>
<p class="center m-5 p-5" style="color:#252525"> Share what you are doing with the community.<br>
<b-button class="button is-dark m-5 p-5" style="background-color:#252525 ;border:none; border-radius:8px;"> Share Activity</b-button></p>
  </div>

</div>

<div class="columns ">
  <div class="column ">
 <div class="card desc p-5 " style="background-color:#252525">
  <div class="card-content">
    <div class="content ">
     <p><b style="color:#ffd65d"> Why Lets Gtok?</b></p><br>
     <p style="color:white">
Lets Gtok aims to provide a safe space online for people to share and connect with genuine feelings. User can share their feelings or activities even without revealing their identity.
     </p>
     <b-button class="button" style="border-radius:8px; background-color:#ffd65d ; border:none">Learn more</b-button>
    </div>
  </div>
</div>
  </div>
  <div class="column">
  <img src="~/assets/image.png" />
  </div>
</div>
<footer>
  
 <div class="card fourth " >
   <div class="card-content">
     
     <div class="content">
       <label>Name</label>
       <b-input type="text" ></b-input>
        <label>E-mail</label>
       <b-input type="text" ></b-input>
        <label>Message</label>
       <b-input type="textarea" ></b-input><br>
       <b-button class="button" style="border-radius:8px; background-color:#ffd65d ; border:none">Submit</b-button>
     </div>
   </div>
 </div>
 
</footer>
</div>
</template>
<script>

export default {
  data(){
    return{
      item:[{heading:"watching", content:'The Wolf of Wall Street. A must Watch I recomend.',user:'@lily', time:'a few seconds ago'},
            {heading:"Watching", content:'The Wolf of Wall Street. A must Watch I recomend.',user:'@lily', time:'a few seconds ago'}],
      item1:[{heading:"Current Feeling", content:'So excited to finally get my hands on the latest PS5',user:'@josh', time:'a few seconds ago'},
      {heading:"Current Feeling", content:'So excited to finally get my hands on the latest PS5',user:'@josh', time:'a few seconds ago'}]
    
    }

  }
}
</script>

<style scoped>
.c1{
  text-align: center;
margin-top: 100px;
margin-bottom: 180px;
padding: 30px;
  /* width: 50%; */
}
.one{
  background-color: #252525;
 padding: 8px;
  border-radius: 8px;
  /* margin: 5px; */
}
.center{
  text-align: center;
  align-items: center;
  justify-content: center;
}
strong{
  text-align: center;
  
}
.column{
 justify-content: center;
display: block;

  align-items: center;
}
.desc{
  margin-top: 150px;
  margin-bottom: 100px;
  margin-left: 150px;
}
.top{
 background-color:#252525
}
.first{

display: flex;
  justify-content: space-evenly;
}

.third{
  background-color: #252525;
  margin: auto;

}
.third2{
background-color: #ffd65d;
}
.fourth{
  width: 50%;
margin: 40px;
}
footer{
  background-color: #252525;
  display: flex;
  justify-content: space-evenly;
}

@media  (max-width: 700px) {
  .c1{
 width: 90%;
}
.desc{
  margin-left: 10px;
  margin-right: 10px;
}
.fourth{
  width: 90%;
margin: 40px;
}
}

</style>