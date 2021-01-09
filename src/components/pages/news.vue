<template>
  <div class="main-container">
    <headers />
    <div class="courses-news">
      <div class="news-heading">
        <h2>NEWS & EVENTS</h2>
      </div>
      <div class="slider">
        <b-carousel
          id="carousel-1"
          v-model="slide"
          :interval="4000"
          controls
          indicators
          background="#ababab"
          img-width="1024"
          img-height="480"
          style="text-shadow: 1px 1px 2px #333;"
          @sliding-start="onSlideStart"
          @sliding-end="onSlideEnd"
        >
          <b-carousel-slide>
            <div class="technology-heading">
              <h3>Nano Technology New updates on fire</h3>
              <p>Indian institute of Technology is invented new technology</p>
              <div class="btn-section">
                <a
                  src="https://eandt.theiet.org/content/articles/2020/07/us-army-lab-finds-safeguards-for-quantum-communications/"
                  class="btn btn-explore"
                >Explore more>></a>
              </div>
            </div>
            <template v-slot:img>
              <img
                class="d-block img-fluid w-100"
                width="900"
                height="300"
                src="../../assets/p20.png"
                alt="image slot"
              />
            </template>
          </b-carousel-slide>
          <b-carousel-slide>
            <div class="technology-heading">
              <h3>Nano Technology New updates on fire</h3>
              <p>Indian institute of Technology is invented new technology</p>
              <div class="btn-section">
              <!-- <button class="btn btn-explore" @click="myfun()">Explore more>></button> -->
                <a
                  href="https://eandt.theiet.org/content/articles/2020/07/us-army-lab-finds-safeguards-for-quantum-communications/"
                  class="btn btn-explore"
                >Explore more>></a>
              </div>
            </div>
            <template v-slot:img>
              <img
                class="d-block img-fluid w-100"
                width="1024"
                height="480"
                src="../../assets/p20.png"
                alt="image slot"
              />
            </template>
          </b-carousel-slide>
        </b-carousel>
      </div>
    </div>
    <div class="heading-second">
      <h1>Suggested Topics</h1>
    
    <div class="courses-news1">
      <div class="box-1">
        <a href="#">
          <img class="news-img" src="@/assets/p6.png" />
        </a>
        <figcaption>
          <a href="#">
        <h2>read more >></h2>
        </a>
        </figcaption>
        <h1>Technology</h1>
      </div>
      <div class="box-1">
        <a href="#">
          <img class="news-img" src="@/assets/p6.png" />
        </a>
         <figcaption>
          <a href="#">
        <h2>read more >></h2>
        </a>
        </figcaption>
        <h1>Job vacancies</h1>
      </div>

      <div class="box-1">
        <a href="#">
          <img class="news-img" src="@/assets/p6.png" />
        </a>
         <figcaption>
           <a href="#">
        <h2>read more >></h2>
        </a>
        </figcaption>
        <h1>Entertainment</h1>
      </div>
    </div>
    </div>
    <div class="courses-news2">
      <div class="news-box">
        <b-row>
          <b-col sm="3">
            <img class="news-img1" src="@/assets/p9.jpg" />
          </b-col>
          <b-col sm="6">
            <h3>
              US Army Lab finds safeguards
              <br />for quantum communications
              <br />
              <br />
              <span class="spical-news">Uploaded 27 July 2020 12.30pm</span>
            </h3>

            <p>Quantum information science is a rapidly growing interdisciplinary field exploring new ways of storing, manipulating and communicating information. Researchers aim to...</p>
            <a
              href="https://eandt.theiet.org/content/articles/2020/07/us-army-lab-finds-safeguards-for-quantum-communications/"
            ></a>
          </b-col>
          <b-col sm="3">
            <span class="spical-icon1">
              <a href="#">
                <b-icon icon="bookmark"></b-icon>
              </a>
            </span>
            <span class="spical-icon2">
              <a href="#">
                <b-icon icon="reply-fill"></b-icon>
              </a>
            </span>
             <a
              href="https://eandt.theiet.org/content/articles/2020/07/us-army-lab-finds-safeguards-for-quantum-communications/"
              class="btn btn-read" 
            >View Details</a>
            <!-- <a  @click="myfun('https://www.youtube.com/')"
              class="btn btn-read"
            >View Details</a> -->
            
             <!-- <button class="btn btn-read" @click="this.window.location='https://www.youtube.com/'" >Explore more>></button> -->
              <!-- <button class="btn btn-read" @click="myfun2()" >Explore more>></button> -->
          </b-col>
        </b-row>
      </div>

      <div class="news-box">
        <b-row>
          <b-col sm="3">
            <img class="news-img1" src="@/assets/p9.jpg" />
          </b-col>
          <b-col sm="6">
            <h3>
              US Army Lab finds safeguards
              <br />for quantum communications
              <br />
              <br />
              <span class="spical-news">Uploaded 27 July 2020 12.30pm</span>
            </h3>

            <p>Quantum information science is a rapidly growing interdisciplinary field exploring new ways of storing, manipulating and communicating information. Researchers aim to...</p>
            <a
              href="https://eandt.theiet.org/content/articles/2020/07/us-army-lab-finds-safeguards-for-quantum-communications/"
            ></a>
          </b-col>
          <b-col sm="3">
            <span class="spical-icon1">
              <a href="#">
                <b-icon icon="bookmark"></b-icon>
              </a>
            </span>
            <span class="spical-icon2">
              <a href="#">
                <b-icon icon="reply-fill"></b-icon>
              </a>
            </span>
            <a
              href="https://eandt.theiet.org/content/articles/2020/07/us-army-lab-finds-safeguards-for-quantum-communications/"
              class="btn btn-read"
            >View Details</a>
          </b-col>
        </b-row>
      </div>
    </div>
     <section class="table">
      <h1>Latest Placement Updates</h1>
     <!-- <div class="table-upadat">
        <b-table striped hover :items="items" :fields="fields"></b-table>
      </div> -->
      <footers />
    </section>
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
  },
  myfun(link){
    let path = link;
    this.$router.push({
      path:path
    });
    // window.location.href= "https://www.youtube.com/"
  }

};
</script>
<style scoped>
.img-fluid {
  width: 37rem;
  height: 23rem;
  background: #017efc;
}
.courses-news {
  background: #017efc 0% 0% no-repeat padding-box;
  display: flex;
  align-content: center;
  flex-direction: column;
  flex-wrap: wrap;
  opacity: 1;
}

.news-heading h2 {
  text-align: center;
  color: white;
  font-family: 'Fjalla One', sans-serif;
  padding-top: 3rem;
  padding-bottom: 2rem;
  font-size: 2rem;
}
.slider {
  height: 24rem;
  width: 47rem;
  margin: 1rem 0 4rem 0;
}
.technology-heading {
  position: relative;
}
.technology-heading h3 {
   font-family: 'Fjalla One', sans-serif;
  font-size: 1.3rem;
  color: #fff;
  text-align: left;
  padding: 1rem 0 0 0;
}
.technology-heading p {
   font-family: 'Fjalla One', sans-serif;
font-family: 'Roboto', sans-serif;
  font-size: 0.9rem;
  color: #fff;
  text-align: left;
  padding: 0 0 11rem 0;
}
.btn-explore {
  padding: .6rem;
  font-size: .8rem;
  color: #0052b8;
  margin: 0 0 1rem 26rem;
  background: #ffffff 0% 0% no-repeat padding-box;
  border-radius: 6px;
    font-family: 'Fjalla One', sans-serif;
font-family: 'Roboto', sans-serif;
box-shadow: none;
}
.courses-news1 {
  
  position: relative;
  display: flex;
  justify-content: center;
  flex-direction: row;
  flex-wrap: wrap;
  opacity: 1;
}
.heading-second{
background: #f8f8f8 0% 0% no-repeat padding-box;
}
.heading-second h1 {
  text-align: center;
  font-size: 2rem;
  padding-bottom: 3rem;
  padding-top: 5rem;
   font-family: 'Fjalla One', sans-serif;
}
.box-1 {
  position: relative;
  height: 15rem;
  width: 17rem;
  margin: 1rem 2rem 5rem 2rem;
  background: #ffffff 0% 0% no-repeat padding-box;
  box-shadow: 0px 6px 9px #00000029;
  border-radius: 6px;
  overflow: hidden;
}
.box-1 h1 {
   font-family: 'Fjalla One', sans-serif;
font-family: 'Roboto', sans-serif;
  text-align: center;
  font-size: 1rem;
}
figcaption{
  position: absolute;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
 opacity: 0;
  display: flex;
  justify-content: center;
  align-items: center;
   font-family: 'Fjalla One', sans-serif;
font-family: 'Roboto', sans-serif;
 font-size: 1rem;
 text-transform: uppercase; 
 transition: all 1s linear; 
}
figcaption h2{
font-size: 1rem;
color: white;

}
.news-img {
  height: 13rem;
  width: 17rem;
  float: left;
  transition: all 1s linear;
}
.box-1:hover .news-img {
  transform: scale(1.1); 
}
.box-1:hover figcaption {
 opacity: 1;
 background: rgba(0,0,0,.3);

}
.latest-news {
  margin-top: 9rem;
}
.courses-news2 {
  margin-top: 9rem;
  display: flex;
  align-items: center;
  flex-direction: column;
  flex-wrap: wrap;
}
.news-box {
  position: relative;
  width: 66rem;
  height: 18rem;
  margin: 2rem;
  background: #ffffff 0% 0% no-repeat padding-box;
  box-shadow: 0px 6px 9px #00000026;
  opacity: 1;
}
.news-box img {
  float: left;
}
.news-img1 {
  width: 17rem;
  height: 18rem;
  float: left;
}
.news-box h3 {
  text-align: left;
  font-size: 1.3rem;
  padding: 1.5rem 0 0 1.5rem;
 font-family: 'Fjalla One', sans-serif;
  letter-spacing: 0px;
}
.spical-news {
  font-size: .9rem;
  text-align: left;
  padding: 0.1rem 0 0 0rem;
   font-family: 'Fjalla One', sans-serif;
font-family: 'Roboto', sans-serif;
}
.news-box p {
  text-align: left;
  font-size: 1rem;
  padding: 1.5rem 0 0 1.5rem;
 font-family: 'Fjalla One', sans-serif;
font-family: 'Roboto', sans-serif;
  letter-spacing: 0px;
}
.btn {
  height: 2.5rem;
  width: 9rem;
}
.btn-read {
  background: #ff9e48 0% 0% no-repeat padding-box;
  border-radius: 5px;
  color: white;
  margin-left: 2.5rem;
  font-size: .9rem;
  padding: .5rem;
  margin-top: 14rem;
   font-family: 'Fjalla One', sans-serif;
font-family: 'Roboto', sans-serif;
}
.news-box .spical-icon1 {
  position: absolute;
  padding-top: 1rem;
  padding-left: 9rem;
  font-size: 2rem;
  color: black;
}
.news-box .spical-icon2 {
  position: absolute;
  padding-top: 8rem;
  padding-left: 9rem;
  font-size: 2rem;
  color: black;
}

.table {
  margin-top: 5rem;
}
.table h1 {
  text-align: center;
  font-size: 2rem;
  letter-spacing: 0px;
  color: #7a7a7a;
   font-family: 'Fjalla One', sans-serif;
}
.table-upadat {
  width: 78%;
  margin-left: 10rem;
}

@media screen and (max-width: 800px) {
  .img-fluid {
    width: 90%;
    height: 16rem;
    background: #017efc;
  }
  .courses-news {
    width: auto;
  }

  .news-heading h2 {
    font-size: 1.5rem;
  }
  .slider {
    height: 16rem;
    width: 90%;
    margin: 1rem 0 2rem 0;
  }
  .technology-heading {
    position: relative;
  }
  .technology-heading h3 {
    font-size: 0.8rem;
    padding: 1rem 0 0 0;
  }
  .technology-heading p {
    font-size: 0.7rem;

    padding: 0 0 4rem 0;
  }
  .btn-explore {
    font-size: 0.8rem;

    margin: 0 0 1rem 1rem;
    background: #ffffff 0% 0% no-repeat padding-box;
  }
  .heading-second h1 {
    font-size: 1.5rem;
    padding-top: 4rem;
    padding-bottom: 0;
  }
  .courses-news1 {
    margin-top: 1rem;
  }
  .box-1 {
    height: 15rem;
    width: 20rem;
    margin: 2rem;
  }
  .box-1 h1 {
  font-size: 1rem;
}
  .news-img {
    margin: .2rem;
  height: 12rem;
  width: 100%;
  float: left;
}
  .courses-news2 {
    position: relative;
    margin-top: 2rem;
    flex-direction: row;
  }
  .news-box {
    position: relative;
    width: 75rem;
    height: 30rem;
    margin: 2rem 1rem 1rem 1rem;
  }
  .news-img1 {
    width: 100%;
    margin: 0;
    height: 10rem;
  }
  .news-box h3 {
    text-align: left;
    font-size: 1rem;
    padding: 1rem 0 0 1rem;
  }
  .spical-news {
    font-size: 0.8rem;
    text-align: left;
  }
  .news-box p {
    text-align: left;
    font-size: 1rem;
    padding: 1rem .5rem 0 1rem;
  }
  .btn-read {
    width: 90%;
    margin: 0 1rem 0.5rem 1rem;
  }
  .spical-icon1 {
    display: none;
  }
  .spical-icon2 {
    display: none;
  }
  .table {
    margin-top: 2rem;
  }
  .table h1 {
    font-size: 1.5rem;
  }
  .table-upadat {
    width: auto;
    margin: 1rem 1rem 1rem 1rem;
  }
}
</style>