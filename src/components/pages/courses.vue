<template>
  <div class="main-container">
    <headers />
    <div class="courses-section">
      <div class="courses-heading">
        <h2>QPARAMS Growth accelerated Trainings</h2>
        <p>
          Our Qparam courses aim to accelerate your career by making you proficient in this domain. We aim to make you proficient in the technology
          field by helping you learn both basic and advanced concepts of new Technologies.
        </p>
      </div>
    </div>
    <div class="heading-second">
      <h2>Courses offering</h2>
    </div>

    <div class="courses-section1">
      <div class="courses-box">
        <b-row>
          <b-col sm="3">
            <img class="mision-img" src="@/assets/p7.png" />
          </b-col>
          <b-col sm="9">
            <b-row>
              <b-col sm="5">
                <h1>Design Verification</h1>
                <span class="populear">
                  <h4>POPULAR</h4>
                  <h2>
                    5
                    <b-icon icon="star-fill"></b-icon>
                  </h2>
                  <h3>10K+ Learners</h3>
                </span>
                <p>System Verilog for advanced Verification ASIC Verification concepts Verification IP Development IP Level Verification Project Lab based assignments</p>
              </b-col>
              <b-col sm="3">
                <span class="courses-project">
                  <p>22 Projects | 166 Hours</p>
                </span>
              </b-col>
              <b-col sm="4">
                <div class="box-clip">
                  <p>
                    <img class="certificate-img" src="@/assets/certificate.svg" /> Certification
                  </p>
                </div>
                <a @click="goTo('details')" class="btn btn-read">View Details</a>
              </b-col>
            </b-row>
          </b-col>
        </b-row>
      </div>

      <div class="courses-box">
        <b-row>
          <b-col sm="3">
            <img class="mision-img" src="@/assets/p4.png" />
          </b-col>
          <b-col sm="9">
            <b-row>
              <b-col sm="5">
                <h1>Physical Designn</h1>
                <span class="populear">
                  <h4>POPULAR</h4>
                   <h2>
                    5
                    <b-icon icon="star-fill"></b-icon>
                  </h2>
                  <h3>10K+ Learners</h3>
                </span>
                <p>System Verilog for advanced Verification ASIC Verification concepts Verification IP Development IP Level Verification Project Lab based assignments</p>
              </b-col>
              <b-col sm="3">
                <span class="courses-project">
                  <p>22 Projects | 166 Hours</p>
                </span>
              </b-col>
              <b-col sm="4">
                <div class="box-clip">
                  <p>
                    <img class="certificate-img" src="@/assets/certificate.svg" /> Certification
                  </p>
                </div>
                <a @click="goTo('details')" class="btn btn-read">View Details</a>
              </b-col>
            </b-row>
          </b-col>
        </b-row>
      </div>
      <div class="courses-box">
        <b-row>
          <b-col sm="3">
            <img class="mision-img" src="@/assets/p3.png" />
          </b-col>
          <b-col sm="9">
            <b-row>
              <b-col sm="5">
                <h1>Static Timing Analysis</h1>
                <span class="populear">
                  <h4>POPULAR</h4>
                   <h2>
                    5
                    <b-icon icon="star-fill"></b-icon>
                  </h2>
                  <h3>10K+ Learners</h3>
                </span>
                <p>System Verilog for advanced Verification ASIC Verification concepts Verification IP Development IP Level Verification Project Lab based assignments</p>
              </b-col>
              <b-col sm="3">
                <span class="courses-project">
                  <p>22 Projects | 166 Hours</p>
                </span>
              </b-col>
              <b-col sm="4">
                <div class="box-clip">
                  <p>
                    <img class="certificate-img" src="@/assets/certificate.svg" /> Certification
                  </p>
                </div>
                <a @click="goTo('details')" class="btn btn-read">View Details</a>
              </b-col>
            </b-row>
          </b-col>
        </b-row>
      </div>

      <div class="courses-box">
        <b-row>
          <b-col sm="3">
            <img class="mision-img" src="@/assets/p6.png" />
          </b-col>
          <b-col sm="9">
            <b-row>
              <b-col sm="5">
                <h1>Design For Test</h1>
                <span class="populear">
                  <h4>POPULAR</h4>
                   <h2>
                    5
                    <b-icon icon="star-fill"></b-icon>
                  </h2>
                  <h3>10K+ Learners</h3>
                </span>
                <p>System Verilog for advanced Verification ASIC Verification concepts Verification IP Development IP Level Verification Project Lab based assignments</p>
              </b-col>
              <b-col sm="3">
                <span class="courses-project">
                  <p>22 Projects | 166 Hours</p>
                </span>
              </b-col>
              <b-col sm="4">
                <div class="box-clip">
                  <p>
                    <img class="certificate-img" src="@/assets/certificate.svg" /> Certification
                  </p>
                </div>
                <a @click="goTo('details')" class="btn btn-read">View Details</a>
              </b-col>
            </b-row>
          </b-col>
        </b-row>
      </div>

      <div class="courses-box">
        <b-row>
          <b-col sm="3">
            <img class="mision-img" src="@/assets/p5.png" />
          </b-col>
          <b-col sm="9">
            <b-row>
              <b-col sm="5">
                <h1>Cloud Computing</h1>
                <span class="populear">
                  <h4>POPULAR</h4>
                  <h2>
                    5
                    <b-icon icon="star-fill"></b-icon>
                  </h2>
                  <h3>10K+ Learners</h3>
                </span>
                <p>System Verilog for advanced Verification ASIC Verification concepts Verification IP Development IP Level Verification Project Lab based assignments</p>
              </b-col>
              <b-col sm="3">
                <span class="courses-project">
                  <p>22 Projects | 166 Hours</p>
                </span>
              </b-col>
              <b-col sm="4">
                <div class="box-clip">
                  <p>
                    <img class="certificate-img" src="@/assets/certificate.svg" /> Certification
                  </p>
                </div>
                <a @click="goTo('details')" class="btn btn-read">View Details</a>
              </b-col>
            </b-row>
          </b-col>
        </b-row>
      </div>
      <div class="courses-box">
        <b-row>
          <b-col sm="3">
            <img class="mision-img" src="@/assets/p8.png" />
          </b-col>
          <b-col sm="9">
            <b-row>
              <b-col sm="5">
                <h1>Embedded and IOT</h1>
                <span class="populear">
                  <h4>POPULAR</h4>
                  <h2>
                    5 <b-icon icon="star-fill"></b-icon>
                  </h2>
                  <h3>10K+ Learners</h3>
                </span>
                <p>System Verilog for advanced Verification ASIC Verification concepts Verification IP Development IP Level Verification Project Lab based assignments</p>
              </b-col>
              <b-col sm="3">
                <span class="courses-project">
                  <p>22 Projects | 166 Hours</p>
                </span>
              </b-col>
              <b-col sm="4">
                <div class="box-clip">
                  <p>
                    <img class="certificate-img" src="@/assets/certificate.svg" /> Certification
                  </p>
                </div>
                <a @click="goTo('details')" class="btn btn-read">View Details</a>
              </b-col>
            </b-row>
          </b-col>
        </b-row>
      </div>
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
.courses-section {
  width: auto;
  background: #017efc 0% 0% no-repeat padding-box;
  display: flex;
  justify-content: center;
  flex-direction: row;
  flex-wrap: wrap;
  opacity: 1;
}
.courses-heading h2 {
  padding-left: 8rem;
  color: white;
  font-family: "Fjalla One", sans-serif;
  padding-top: 8rem;
  font-size: 2rem;
}
.courses-heading p {
  text-align: left;
  padding: 1.5rem 9rem 8rem 8rem;
  font-family: 'Fjalla One', sans-serif;
font-family: 'Roboto', sans-serif;
  color: white;
  font-size: 1.3rem;
}
.heading-second h2 {
  position: relative;
  color: #7a7a7a;
   font-family: "Fjalla One", sans-serif;
  text-align: left;
  padding-top: 5rem;
  padding-left: 8rem;
  font-size: 2rem;
}
.courses-section1 {
  margin-top: 1rem;
  position: relative;
  display: flex;
  align-items: center;
  flex-direction: column;
  flex-wrap: wrap;
}

.courses-box {
  width: 68rem;
  height: 18rem;
  background-color: #ffffff;
  margin: 3rem;
  box-shadow: 0px 4px 6px #0000000f;
  border-radius: 12px;
}
.mision-img {
  width: 17rem;
  height: 19rem;
  float: left;
  clip-path: polygon(0 0, 100% 0, 100% 100%, 46% 100%, 30% 85%, 0 58%);
}

.courses-box h1 {
  text-align: left;
  display: inline-block;
  font-size: 1.5rem;
  padding-top: 2rem;
 font-family: "Fjalla One", sans-serif;
  letter-spacing: 0px;
  color: #7a7a7a;
}
.courses-box p {
  padding-top: 2rem;
  text-align: left;
  font-size: 1rem;
  letter-spacing: 0px;
  color: #7a7a7a;
  opacity: 1;
}
.courses-project p {
  margin-top: 9rem;
  font-size: 1rem;
  color: #7a7a7a;
}
.box-clip {
  background: #ffffff 0% 0% no-repeat padding-box;
  box-shadow: 0px -2px 6px #0000000d;
  margin-top: 2rem;
  width: 10rem;
  float: right;
  clip-path: polygon(100% 0%, 100% 51%, 100% 100%, 25% 100%, 0% 50%, 25% 0%);
}
.box-clip p {
 color: #7A7A7A;
  padding-top: 1rem;
  float: right;
}
.certificate-img {
  width: 2rem;
  height: 2rem;
}
.btn {
  height: 2.5rem;
  width: 9rem;
}
.btn-read {
  background: #ff9e48 0% 0% no-repeat padding-box;
  border-radius: 5px;
  color: white;
  margin-left: 2.8rem;
  margin-top: 7rem;
  font-size: .9rem;
  padding: .5rem;
   font-family: 'Fjalla One', sans-serif;
font-family: 'Roboto', sans-serif;
}
.populear {
  display: inline-block;
}
.populear h2 {
  display: inline-block;
  font-size: .9rem;
  background: #ff9e48 0% 0% no-repeat padding-box;
  border-radius: 13px;
  height: 1.5rem;
  width: 3rem;
  padding-top: 0.2rem;
  padding-left: .8rem;
  margin-left: 1rem;
  color: white;
}
.populear h3 {
  display: inline-block;
  font-size: 0.9rem;

  padding-top: 0.1rem;
  padding-left: 1rem;
  margin-left: 1rem;
  color: #7A7A7A;
}
.populear h4 {
  display: inline-block;
  font-size: 0.7rem;
  background: #d81d4a 0% 0% no-repeat padding-box;
  border-radius: 13px;
  height: 1.5rem;
  width: 5.2rem;
  padding-top: 0.4rem;
  padding-left: 0.8rem;
  color: white;
}
.courses-section2 {
  margin-top: 1rem;
}

@media screen and (max-width: 800px) {
  .courses-heading h2 {
    padding-left: 2rem;
    color: white;
    padding-top: 1.5rem;
    font-size: 1.3rem;
  }
  .courses-heading p {
    text-align: left;
    padding: 1rem 1rem 1rem 2rem;
    font-size: 1rem;
  }
  .heading-second h2 {
    text-align: center;
    padding-left: 0;
    padding-top: 2rem;
    font-size: 1.8rem;
  }
  .courses-section1 {
    margin-top: 2rem;
    position: relative;
    flex-direction: row;
  }
  .courses-box {
    width: 70rem;
    height: 33rem;
    margin: 1rem;
  }
  .mision-img {
    width:96%;
    height: 11rem;
    clip-path: none;
    margin: 0 1rem 0 .5rem;
    z-index: -1rem;
  }
  .courses-box h1 {
    text-align: left;
    display: inline-block;
    font-size: 1.5rem;
    padding: 1rem 0 0 1rem;

    letter-spacing: 0px;
    color: #7a7a7a;
  }
  .courses-box p {
    padding: 1rem 0.2rem 0 1rem;

    font-size: 1rem;
  }
  .populear {
    display: inline-block;
  }
  .populear h2 {
    display: inline-block;
    margin-left: 1rem;
    padding-left: 1rem;
    font-size: .8rem;
  }
  .populear h3 {
    display: inline-block;

    margin-left: 1rem;
  }
  .populear h4 {
    display: inline-block;

    margin-left: 1rem;
  }
  .courses-project p {
    margin-top: 0.1rem;
    padding: 0 0 0 5rem;
    font-size: 1rem;
  }
  .box-clip {
    display: none;
  }
  .btn-read {
    padding: 0.5rem;
    font-size: 0.9rem;
    margin-left: 6rem;
    margin-top: 0.1rem;
  }
}
</style>