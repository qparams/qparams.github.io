<template>
  <div class="main-container">
    <headers />
    <div class="contact-section">
      <div class="contact-heading">
        <h2>CONTACT US</h2>
       <p>Suggestions,Questions or Comments Reach out to us .We'd be happy to help</p>
      </div>
    </div>
    <div class="placement-offers">
      <div class="box-1">
        <img class="palcement-img" src="@/assets/p6.png" />
        <span class="populear">
          <p>POPULAR</p>
          <h1>
            5
            <b-icon icon="star-fill"></b-icon>
          </h1>
          <h2>10K+ Learners</h2>
        </span>
        <hr class="line" />

        <a @click="goTo('contact')" class="btn btn-read">Know more&raquo;</a>
      </div>
      <div class="box-2">
        <h1>
          Start your VLSI career with placement assistance
        </h1>
        <p>
          Job oriented Online Embedded system
          <br />and IOT Courses
        </p>
        <a @click="goTo('contact')" class="btn btn-orainge">To Register&raquo;</a>
      </div>
    </div>
    <div class="contact-query">
      <h1>
        If you get any questions
        <br />Please do not hesitate to send us a message
      </h1>
    </div>
    <div class="contact-box">
          <div class="form-group1">
            <b-form @submit="onSubmit" @reset="onReset" v-if="show">
              <b-form-group id="input-group-1" label-for="input-1">
                <b-form-input
                  id="input-1"
                  v-model="form.firstName"
                  required
                  placeholder="First Name"
                ></b-form-input>
              </b-form-group>

              <b-form-group id="input-group-2" label-for="input-2">
                <b-form-input id="input-2" v-model="form.lastName" required placeholder="Last Name"></b-form-input>
              </b-form-group>

              <b-form-group id="input-group-3" label-for="input-3">
                <b-form-input
                  id="input-3"
                  v-model="form.email"
                  type="email"
                  required
                  placeholder="Enter email"
                ></b-form-input>
              </b-form-group>

              <b-form-group id="input-group-4" label-for="input-4">
                <b-form-input id="input-4" v-model="form.phone" required placeholder="Phone number"></b-form-input>
              </b-form-group>

              <b-form-group id="input-group-5" label-for="input-5">
                <b-form-select id="input-5" v-model="form.learn" :options="learns" required></b-form-select>
              </b-form-group>
              <b-form-group id="input-group-6" label-for="input-6">
                <b-form-select id="input-6" v-model="form.learn1" :options="learns1" required></b-form-select>
              </b-form-group>
        
              <b-form-group id="input-group-7" label-for="input-7">
                <b-form-input
                  id="textarea"
                  v-model="form.text"
                  required
                  placeholder="Enter something..."
                  rows="3"
                  max-rows="6"
                ></b-form-input>
              </b-form-group>

              <b-form-group id="input-group-8">
                <b-form-checkbox-group v-model="form.checked" id="checkboxes-8">
                  <b-form-checkbox value="accepted">
                    I accept QPARAMS terms and
                    conditions
                  </b-form-checkbox>
                </b-form-checkbox-group>
              </b-form-group>
              

              <b-button type="submit" variant="primary" @click="addToApi">Submit</b-button>
              
            </b-form>
          </div>
       
          <div class="blue">
            <h2>HEADQUARTERS</h2>
            <p>
              Qparams Technologies Pvt Ltd #1, saroj Square, 1st floor Silver Spring Rd, Munnekalal, Marathahalli, Bangaluru, Karnataka 560036
              <br />+91 7676708195
            </p>
            <h2>EMAIL US</h2>
            <p>
              info@qparams.com
              <br />Anusha@qparams.com
            </p>
          </div>
          </div>
        
  
    <div class="google-map">
      <h2>To reach to our destination</h2>
      <iframe
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3888.3055641084225!2d77.70980911413498!3d12.952288718807873!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3bae13f7f289253b%3A0x86fa1f5eea62a05f!2sQparams%20Technologies%20Pvt%20Ltd!5e0!3m2!1sen!2sin!4v1597343826641!5m2!1sen!2sin"
        width="1175"
        height="450"
        frameborder="0"
        style="border:0;"
        allowfullscreen
        aria-hidden="false"
        tabindex="0"
      ></iframe>
    </div>
    <footers />
  </div>
</template>
<script>
import headers from "@/components/layout/header.vue";
import footers from "@/components/layout/footer.vue";
import axios from 'axios';
export default {
  components: {
    headers,
    footers
  },
  data() {
    return {
      form: {
        firstName:"",
        lastName:"",
        email: "",
        phone: "",
        learn: null,
        learn1: null,
        text:"",
        checked: []
      },
      learns: [
        { text: "Select learning mode", value: null },
        "ONLINE",
        "OFFLINE"
      ],
      learns1: [
        { text: "Select your area of interest", value: null },
        "Design Verification",
        "Physical Design",
        "Static Timing Analysis",
        "Design For Test",
        "Cloud Computing",
        "Embedded and IOT"
      ],
      show: true
    };
  },
  methods: {
    onSubmit(evt) {
      evt.preventDefault();
      // alert(JSON.stringify(this.form));
    },
    addToApi(){
      let newform = {
        firstName:this.form.firstName,
        lastName:this.form.lastName,
        email: this.form.email,
        phone: this.form.phone,
        learn: this.form.learn,
        learn1: this.form.learn1,
        text:this.form.text,
        checked: [this.form.checked]

      }
      console.log(newform);
      axios.post('http://localhost:3000/posts',newform).then( (response)=>{
        console.log(response);
      })
      .catch((error)=>{
        console.log(error);

      });
      alert("Your Request successfully submited");
    


    },
    onReset(evt) {
      evt.preventDefault();
      // Reset our form values
      this.form.email = "";
      this.form.firstName = "";
      this.form.lastName = "";
      this.form.phone = "";
      this.form.learn = null;
      this.form.learn1 = null;
      this.form.text = "";
      this.form.checked = [];
      // Trick to reset/clear native browser form validation state
      this.show = false;
      this.$nextTick(() => {
        this.show = true;
      });
    }
  }
};
</script>
<style scoped>
.contact-section {
  background: #FF9E48 0% 0% no-repeat padding-box;
  display: flex;
  justify-content: center;
  flex-direction: row;
  flex-wrap: wrap;
  opacity: 1;
}
.contact-heading {
  width: auto;
}
.contact-heading h2 {
  text-align: center;
  font-style: bold;
  color: white;
  font-family: 'Fjalla One', sans-serif;
  padding-top: 7rem;
  font-size: 2rem;
}
.contact-heading p {
  text-align: center;
  font-size: 1.3rem;
  padding-top: 2rem;
  padding-bottom: 8rem;
  color: white;
   font-family: 'Fjalla One', sans-serif;
font-family: 'Roboto', sans-serif;
}
.contact-query h1 {
  font-size: 1.8rem;
  text-align: left;
  margin-left: 7rem;
  margin-top: 7rem;
font-family: 'Fjalla One', sans-serif;
  letter-spacing: 0px;
  color: #7a7a7a;
  opacity: 1;
}
.contact-box {
  margin:3rem 7rem 0 7rem;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  opacity: 1;
  background: #FFFFFF 0% 0% no-repeat padding-box;
box-shadow: 0px 3px 9px #00000026;
opacity: 0.9;
}
.form-group1{
  width:31rem;
  height:23rem;
  margin:1rem 1rem 1rem 3rem;
 
}
.blue {
  
  background: transparent linear-gradient(312deg, #017efc 0%, #0052b8 100%) 0%
    0% no-repeat padding-box;
  box-shadow: 0px 6px 9px #00000026;
  width:45.5%;
  height: 25rem;
  float: right;
  margin:0 0 0 3.3rem;
 
}
.blue h2 {
  padding: 2rem ;
  font-size: 1.3rem;
  text-align: center;
  color: #ffffff;
    font-family: 'Fjalla One', sans-serif;
}
.blue p {
  padding: 0.1rem .5rem .2rem .5rem;
  font-size: .9rem;
  text-align: center;
  color: #ffffff;
   font-family: 'Fjalla One', sans-serif;
font-family: 'Roboto', sans-serif;
}
.google-map {
  margin-top: 3rem;
  display:flex;
  flex-direction:row;
  flex-wrap:wrap;
}
.google-map h2 {
  text-align: center;
  padding:4rem 0 2rem 7rem;
font-size: 2rem;
  letter-spacing: 0px;
  font-family: 'Fjalla One', sans-serif;
  color: #7a7a7a;
  opacity: 1;
}
.google-map iframe {
  margin:0 6.5rem 0  7rem;
  width: 100%;
}
#input-group-1 {
  width: 14rem;
  display: inline-block;
}
#input-group-2 {
  width: 14rem;
  display: inline-block;
  margin: 1rem;
}
#input-group-3 {
  width: 14rem;
  display: inline-block;
}
#input-group-4 {
  width: 14rem;
  margin: 1rem;
  display: inline-block;
}
#input-group-5 {
  width: 14rem;
  display: inline-block;
  margin-top: 1rem;
}
#input-group-6 {
  width: 14rem;
  margin-left: 1.1rem;
  margin-top: 1rem;
  display: inline-block;
}
#input-group-7 {
  display: inline-block;
  width: 14rem;
}
#input-group-8 {
  display: inline-block;
  margin: 1rem;
  font-size: .6rem;
}
.btn-primary{
  width: 13rem;
  margin: 1rem 0 0 7rem;
  border: none;
  color: #fff;
  background: #364E61 0% 0% no-repeat padding-box;
border-radius: 5px;
opacity: 1;
}
.form-control {
    display: block;
    width: 100%;
    height: calc(1.5em + 0.75rem + 2px);
    padding: 0.375rem 0.75rem;
    font-size: .9rem;
    font-weight: 400;
    line-height: 1.5;
    color: #495057;
    background-color: #fff;
    background-clip: padding-box;
    border: 1px solid #ced4da;
    border-radius: 0.25rem;
    transition: border-color 0.15s ease-in-out, box-shadow 0.15s ease-in-out;
}
.custom-select {
    display: inline-block;
    width: 100%;
    height: calc(1.5em + 0.75rem + 2px);
    padding: 0.375rem 1.75rem 0.375rem 0.75rem;
    font-size: .89rem;
    font-weight: 400;
    line-height: 1.5;
    color: #495057;
   
}

.placement-offers {
  margin-top: 4rem;
  margin-top: 7rem;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  opacity: 1;
}
.palcement-img {
  height: 12rem;
  width: 20rem;
}
.populear {
  display: inline-block;
}
.populear h1 {
  display: inline-block;
  font-size: .8rem;
  background: #ff9e48 0% 0% no-repeat padding-box;
  border-radius: 13px;
  height: 1.5rem;
  width: 3rem;
  padding-top: 0.3rem;
  padding-left: .9rem;
  margin-left: 1rem;
  margin-top: 1rem;
  color: white;
}
.populear h2 {
  display: inline-block;
  font-size: .9rem;

  padding-top: 0.1rem;
  padding-left: 1rem;
  margin-left: 1rem;
  margin-top: 1rem;
  color: #7A7A7A;
}
.populear p {
  display: inline-block;
  font-size: 0.7rem;
  background: #d81d4a 0% 0% no-repeat padding-box;
  border-radius: 13px;
  height: 1.5rem;
  width: 5.2rem;
  padding-top: 0.1rem;
  padding-left: 0.8rem;
  margin-left: 1rem;
  margin-top: 1rem;
  color: white;
}
.btn {
  height: 2.5rem;
  width: 9rem;
  border-radius: 4px;
}
.btn-read {
  position: relative;
   font-size: .9rem;
  padding: .5rem;
  width: 12rem;
  color: #ffffff;
  background: #4bc947 0% 0% no-repeat padding-box;
  border-radius: 4px;
  margin-left: 4rem;
  z-index: 1;
  overflow: hidden;
     font-family: 'Fjalla One', sans-serif;
font-family: 'Roboto', sans-serif;
}
.btn-read::before {
  position: absolute;
  content: "";
  left: 0;
  top: 0;
  background: #d81d4a;
  width: 100%;
  height: 100%;
  border-radius:4px;
transform: translateX(-100%);
transition: all 1s linear;
z-index: -1;
}
.btn-read:hover::before {
transform: translateX(0);
}
.btn-orainge {
  font-size: .9rem;
  padding: .5rem;
  color: #ffffff;
  background: #ff9e48 0% 0% no-repeat padding-box;
  border-radius: 4px;
  margin-top: 2rem;
     font-family: 'Fjalla One', sans-serif;
font-family: 'Roboto', sans-serif;
}
.box-1 {
  height: 21rem;
  width: 20rem;
  margin-left: 10rem;
  
  background: #ffffff 0% 0% no-repeat padding-box;
  box-shadow: 0px 3px 6px #00000036;
  opacity: 1;
 
}
.box-2 {
  margin: 0 0 0 2rem; 
}
.box-2 h1 {
  text-align: left;
  font-size: 2rem;
  letter-spacing: 0px;
  color: #d81d4a;
  text-shadow: 0px 3px 6px #910b2b3d;
   font-family: 'Fjalla One', sans-serif;
}
.box-2 p {
  text-align: left;
  font-size: 1.3rem;
  letter-spacing: 0px;
  color: #7a7a7a;
   font-family: 'Fjalla One', sans-serif;
font-family: 'Roboto', sans-serif;
  opacity: 1;
}

@media screen and (max-width: 800px) {
 .contact-heading h2 {
  padding-top: 2rem;
  font-size: 1.5rem;
}
.contact-heading p {
  font-size: 1rem;
  padding: 1rem 1rem 3rem 1rem;
}
.contact-query h1 {
  font-size: 1.5rem;
  text-align: left;
  margin-left: 2rem;
  padding-right: 1rem;
  margin-top: 3rem;

}
.contact-box {
  margin-top:3rem;
   margin:3rem 1rem 0 1rem;
  

}
.form-group1{
  width:auto;
  height:20rem;
  margin:1rem 0 0 1rem;
}
#input-group-1 {
  margin-left: 2rem;
  margin-top: .5rem;
  width:15rem;
}
#input-group-2 {

  margin-left: 2rem;
  margin-top:.5rem;
  width:15rem;
}
#input-group-3 {
 margin-left: 2rem;
 margin-top:.5rem;
 width:15rem;
}
#input-group-4 {
 margin-left: 2rem;
 margin-top:.5rem;
 width:15rem;
  
}
#input-group-5 {
 margin-top:.5rem;
  margin-left: 2rem;
  width:15rem;
}
#input-group-6 {
margin-left: 2rem;
margin-top:.5rem;
width:15rem;

 
}
#input-group-7 {
  margin-left: 2rem;
  margin-top:.5rem;
 width:15rem;
}
#input-group-8 {
  margin-left: 2rem;
  margin-top: .5rem;
}
#submit-button{
  margin-left:6rem;

}
.blue {
  width: auto;
  height: 25rem;
  margin:16rem 1rem 1rem 1rem;
}
.blue h2 {
  padding: 2rem 1rem 1rem 1rem;
  font-size: 1.3rem;
}
.blue p {
  padding: 0.1rem .5rem .5rem .5rem;
  font-size: 1rem;
}
.btn-primary{
  width: 13rem;
  margin: 1rem 0 0 2.5rem;
}
.google-map {
  margin-top: 2rem;
 
}
.google-map h2 {
  text-align: center;
  margin-left: 2rem;
  padding:2rem 0 2rem 0;
  font-size: 1.5rem;

}
.google-map iframe {
  margin: 1rem 1rem 0 1rem;
  width:100%;
  height:12rem;
}

.placement-offers {
  margin-top: 4rem;
  
}
.palcement-img {
  height: 12rem;
  width: 96%;
  margin: .5rem;
}
.btn-read {
  background: #4bc947 0% 0% no-repeat padding-box;
  border-radius: 4px;
  margin:0 .6rem 0 .6rem;
  width: 43%;
}
.btn-orainge {
  width: 40%;
   position:absolute;
  background: #ff9e48 0% 0% no-repeat padding-box;
  border-radius: 4px;
  margin-top: 18.7rem;
  left:12rem;
}
.box-1 {
  height: 22rem;
  width:100%;
  margin:0 1rem 0 1rem; 
}
.box-2 {
  margin: 0 0 0 2rem;
   order:-1; 
}
.box-2 h1 {
  text-align: left;
  font-size: 1.2rem;
 
}
  
.box-2 p {
 display:none;
}
}
</style>