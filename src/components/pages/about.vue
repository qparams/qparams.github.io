<template>
  <div class="main-container">
    <headers />
    <div class="about-section">
      <div class="about-heading">
            <h2>WHO WE ARE</h2>
            <p>
              “Q Params” is the Corporate and Private Trainings, offering quality training and certifications across India.
             “Q Params Technologies” stands an Institute that never compromises in its Quality Training.
             A group of highly skilled and experienced engineers worked in reputed companies and having
              knowledge in all aspect of VLSI design will be guiding aspirants.
            </p>        
      </div>
<div class="index-box">
        <b-row>
          <b-col col="4" sm="3">
            <img class="vision-img" src="@/assets/vision.svg" />
          </b-col>
          <b-col col="8" sm="9">
            <p>
              Our Vison is to create high Quality tool of hardware engineers by
              <br />giving practical industry level training to students.
            </p>
          </b-col>
        </b-row>
    </div>
      <div class="index-box1">
        <b-row>
          <b-col col="4" sm="3">
            <img class="mision-img" src="@/assets/mission.svg" />
          </b-col>
          <b-col col="8" sm="9">
            <p>QPARAM is the only training institute where all the course contents are<br> mentored by the working professions from semiconductor industry.</p>
          </b-col>
        </b-row>
    </div>
      </div>
  <div class="change-about">
    <div class="change-img">
      <img class="vision1-img" src="@/assets/vision.svg" />
      </div>
      <div class="paragraf-change">
        <p>
              Our Vison is to create high Quality tool of hardware engineers by
              giving practical industry level training to students.
            </p>
        </div>
         <div class="change-img1">
      <img class="vision1-img" src="@/assets/mission.svg" />
      </div>
      <div class="paragraf-change">
        <p>QPARAM is the only training institute where all the course contents are mentored by the working professions from semiconductor industry.</p>
        </div>
    </div>
    <div class="extra-section">
      <div class="heading-extra">
        <h2>WHO WE ARE</h2>
         <p>
              “Q Params” is the Corporate and Private Trainings, offering quality training and certifications across India.
             “Q Params Technologies” stands an Institute that never compromises in its Quality Training.
             A group of highly skilled and experienced engineers worked in reputed companies and having
              knowledge in all aspect of VLSI design will be guiding aspirants.
            </p>    
        </div>
      </div>
  <div class="heading-second"> <h2>OUR FOUNDERS</h2>
    <div class="about-section1">
      <div class="about-box">
        <b-row>
          <b-col sm="4">
            <img class="mision-img" src="@/assets/p2.png" />
          </b-col>
          <b-col sm="8">
            <h2>Zonai Haris</h2>
            <h3>Co-Founder MD</h3>
            <p>
              "I got placed as Embedded Engineer in Qualcomm which is
              the most memorable moment of my life. Every Embedded
             Engineer would have dreamt of joining a company like
             Qualcomm but I was able to fulfill this dream with the
              immense support of Qparams."
            </p>
          </b-col>
        </b-row>
      </div>
      <div class="about-box">
        <b-row>
          <b-col sm="4">
            <img class="mision-img" src="@/assets/p2.png" />
          </b-col>
          <b-col sm="8">
            <h2>Zonai Haris</h2>
            <h3>Co-Founder MD</h3>
             <p>
              "I got placed as Embedded Engineer in Qualcomm which is
              the most memorable moment of my life. Every Embedded
             Engineer would have dreamt of joining a company like
             Qualcomm but I was able to fulfill this dream with the
              immense support of Qparams."
            </p>
          </b-col>
        </b-row>
       </div>
        </div>
        </div>
         <div class="heading-second1"> <h2>Placements</h2></div>
    <div class="about-section3">
      <div class="about-placement">
      <h2>
        Placement are integrated part of our training program
        Dedicated team of experienced HR's are successful in
        bringing better opportunity to our Students.
      </h2>
      <a  @click="goTo('placement')" class="btn btn-read">Know more</a>
      </div>
 <!-- <div class="center-img">
      <img class="placement-img" src="@/assets/p2.png" />
    </div> -->
    
    </div>
    <footers />
  </div>
</template>
<script>
import headers from "@/components/layout/header.vue";
import footers from "@/components/layout/footer.vue";
export default {
  components: {
    headers,
    footers
  },
   methods: {
    goTo(page) {
      let path = "/" + page;
      this.$router.push({
        path: path
      });
    }
   }
};
</script>
<style scoped>
.about-section {
  position:relative;
  width: auto;
  background: #fcac66 0% 0% no-repeat padding-box;
  
 display: flex;
  align-content: center;
  flex-direction: column;
  flex-wrap: wrap;
  opacity: 1;
}
.about-heading{
  width: 61rem;
}
.about-heading h2 {
  text-align: center;
  color: white;
  font-family: 'Fjalla One', sans-serif;
  padding: 5rem 0 0 0;
  font-size: 2rem;
}
.about-heading p {
  text-align:center;
  color: white;
   font-family: 'Fjalla One', sans-serif;
font-family: 'Roboto', sans-serif;
  padding: 3rem 0 18rem 0;
  font-size: 1.3rem;
}
.index-box {
  position: absolute;
  width: 70rem;
  height: 8rem;
    top:70%;
    left: 50%;
      transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  z-index: 1;
  background: #ffffff 0% 0% no-repeat padding-box;
  box-shadow: 0px 3px 6px #0000001f;
  border-radius: 10px;
  opacity: 1;
}
.index-box img {
  justify-content: center;
  align-items: center;
  margin-top: 1rem;
  margin-left: 3rem;
  width: 6rem;
}
.index-box p {
  text-align: left;
  font-size: 1.2rem;
  padding-top: 2rem;
  letter-spacing: 0px;
   font-family: 'Fjalla One', sans-serif;
font-family: 'Roboto', sans-serif;
  color: #7a7a7a;
  opacity: 1;
}
.index-box1 {
  position: absolute;
   width: 70rem;
  height: 8rem;
    top:100%;
    left: 50%;
      transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  z-index: 1;
  background: #ffffff 0% 0% no-repeat padding-box;
  box-shadow: 0px 3px 6px #0000001f;
  border-radius: 10px;
  opacity: 1;
}
.index-box1 img {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 1rem;
  margin-left: 3rem;
  width:6rem ;
}
.index-box1 p {
  text-align: left;
  font-size: 1.2rem;
  padding-top: 2rem;
  letter-spacing: 0px;
  color: #7a7a7a;
   font-family: 'Fjalla One', sans-serif;
font-family: 'Roboto', sans-serif;
  opacity: 1;
}
.change-about{
  display: none;
}
.extra-section{
   display: none;
}
.about-section1 {
  margin-top: 1rem;
  display: flex;
  justify-content: center;
  flex-direction: row;
  flex-wrap: wrap;
}
.heading-second{
background-color: #fcfcfc;
}
.heading-second h2 {
  color: #7A7A7A;
  text-align: center;
  font-family: 'Fjalla One', sans-serif;
  padding-top: 9rem;
  font-size: 2rem;
}
.heading-second1 h2 {
  text-align: center;
  font-family: 'Fjalla One', sans-serif;
  color: #7A7A7A;
  padding-top: 7rem;
  font-size: 2.2rem;
}
.about-box {
  width: 45rem;
  height: 19rem;
  background-color: #ffffff;
  margin: 4rem;
  box-shadow: 0px 8px 0px #017efc;
  border: 1px solid #7070702b;
  border-radius: 19px;
}

.about-box img {
  border-radius: 50%;
  width: 8rem;
  height: 8rem;
  margin-left: 2rem;
  margin-top: 2rem;
}
.about-box h2 {
  text-align: left;
   font-family: 'Fjalla One', sans-serif;
font-family: 'Roboto', sans-serif;
  font-size: 1.5rem;
  padding-top: 2rem;

  letter-spacing: 0px;
  color: #364e61;
}
.about-box h3 {
  text-align: left;
  font-size: 1rem;
  letter-spacing: 0px;
  color: #364e61;
  opacity: 1;
}
.about-box p {
  text-align: left;
  padding: 1rem 8rem 0 0 ;
  font-size: 1rem;
  font-style: italic;
   font-family: 'Fjalla One', sans-serif;
font-family: 'Roboto', sans-serif;
  letter-spacing: 0px;
  color: #364e61;
  opacity: 1;
}

.about-section3 {
     position: relative;
    background-image: url("../../assets/p2.png");
    background-size: 100% 100%;
 display: flex;
  justify-content: center;
  flex-direction: row;
  flex-wrap: wrap;
  margin: 3rem 15rem 1rem 15rem;
  height:75vh;
}
.about-placement {
  position: relative;
}
.about-placement h2 {
  font-size: 1.5rem;
  text-align: center;
  padding: 5rem 4rem 4rem 4rem;
  line-height: 1.5;
  color: white;
  font-style: italic;
   font-family: 'Fjalla One', sans-serif;
font-family: 'Roboto', sans-serif;
  z-index: 1;
}
.btn {
  height: 2.5rem;
  width: 9rem;
  border-radius: 4px;
}
.btn-read {
  background: #ffffff 0% 0% no-repeat padding-box;
  color: #364e61;
  border-radius: 4px;
   position: absolute;
    top:85%;
    left: 50%;
      transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  font-size: .9rem;
   font-family: 'Fjalla One', sans-serif;
font-family: 'Roboto', sans-serif;
overflow: hidden;
}
.btn-read::before {
  position: absolute;
  content: "";
  left: 0;
  top: 0;
  background: #fcac66;
  width: 100%;
  height: 100%;
  border-radius:4px;
transform: translateX(-100%);
transition: all .8s linear;
z-index: -1;
}
.btn-read:hover::before {
transform: translateX(0);
}
@media screen and (max-width: 800px) {
 .about-heading{
   position: relative;
  width:100%;
  display: none;
}
 .about-heading h2 {
  padding-top: 20rem;
  font-size: 1.5rem;
 
}
.about-heading p {
  color: white;
  padding: 1rem ;
  font-size: .9rem;
  
}
.index-box {
   display: none;
  position: absolute;
    background: #fcac66 0% 0% no-repeat padding-box;
   width: 100%;
  height: auto;
  position: absolute;
  z-index: 0;
  top: 20%;
  left: 50%;
   box-shadow: none;
   border-radius:0;
  

}
.index-box img {
  justify-content: center;
  align-items: center;
  margin-top: 2rem;
  margin-left: 1rem;
  width:7rem;
  height:7rem;
  color: white;
}
.index-box p {
  font-size: 1rem;
  padding-top: .5rem;
}
.index-box1 {
   display: none;
  position: absolute;
  width: auto;
  height: auto;
  top: 38rem;
  left: 1rem;
  right:1rem;

}
.index-box1 img {
  justify-content: center;
  align-items: center;
  margin-top: 2rem;
  margin-left: 1rem;
  width:7rem;
  height:7rem;
}
.index-box1 p {
  font-size: 1rem;
  padding-top: .5rem;
}
.change-about{
  position: relative;
  display: flex;
  flex-direction: column;
  align-content: center;
  flex-wrap: wrap;
   background: #fcac66 0% 0% no-repeat padding-box;
}
.change-img{
  position: absolute;
   background:#fff;
  border-radius: 50%;
  width: 6rem;
  height: 6rem;
   top:18%;
    left: 50%;
      transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
}
.change-img1{
  position: absolute;
   background:#fff;
  border-radius: 50%;
  width: 6rem;
  height: 6rem;
   top:66%;
    left: 50%;
      transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
}
.vision1-img{
  width: 4rem;
  margin: 1rem 0 0 1rem;
 
}
.paragraf-change p{
  font-size: .9rem;
  padding: 10rem 2rem 0 2rem;
  color: #fff;
  text-align: center;
}
.extra-section{
   position: relative;
  display: flex;
  flex-direction: column;
  align-content: center;
  flex-wrap: wrap;

}
.heading-extra{
  width: 90%;
  height: auto;
  margin: 4rem 1rem 1rem 1rem;
  background: #ffffff 0% 0% no-repeat padding-box;
  box-shadow: 0px 3px 6px #00000073;
  border-radius: 10px;
}
.heading-extra h2{
  padding: 1rem;
  font-size: 1.5rem;
  color: #FF9E48;
  text-align: center;
}
.heading-extra p{
  padding: 1rem;
  font-size: 1rem;
  color: #FF9E48;
  text-align: center;
}
.about-section1 {
  position: relative;
  margin-top: 1rem;
   flex-direction: row;
 
}
.heading-second h2 {
  padding-top: 2rem;
  font-size: 1.5rem;
}
.about-box {
  width: 55rem;
  height: 25rem;
  background-color: #ffffff;
  margin: 1rem 1rem 1rem 1rem; 
}
.about-box img {
  border-radius: 50%;
  width: 6rem;
  height: 6rem;
  position: relative;
}
.mision-img{
  position: absolute;
    top:25%;
    left: 40%;
      transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
}
.about-box h2 {
  font-size: 1.2rem;
  padding-top: 1rem;
  padding-left:7rem;
}
.about-box h3 {
  text-align: left;
  font-size: .9rem;
   padding-left:7rem;
  
}
.about-box p {
  text-align: center;
  font-size: .9rem;
  padding: 1rem 1rem 0 1rem ;
  
}
.heading-second1 h2 {
  text-align: center;
  padding-top: 2rem;
}
.about-section3 {
  margin: 2rem 1rem 1rem 1rem;
  height:40vh;
}
.about-placement h2 {
  font-size: 1.1rem;
  padding: 2rem 1rem 0 1rem;
  
}
.btn-read {
   position: absolute;
    top:86%;
    left: 50%;
      transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
margin: 0;
}
}
</style>