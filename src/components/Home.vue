<template>
    <div>
      <Navbar/>      
      <div class="appBodyCover">
        <img src="../assets/6.jpg" alt="">
        <div class="quote">
          <h1>Sunset Lodge Hotel, Colombo</h1>
          <h3>Set on the Galle Face Promenade overlooking the Indian Ocean, this upmarket hotel is surrounded by high-end shopping and dining. It's a 6-minute walk from Galle Face Green urban park and 2 km from Beira Lake.
            Featuring city, lake or ocean views, the refined rooms offer free Wi-Fi, flat-screen TVs, and tea and coffee-making facilities, plus minibars. Upgraded rooms add balconies. Suites offer separate living rooms and access to a club lounge.</h3>
        </div>
      </div>
      <hr class="horizantalLine">
      
      <div class="sectionTwo">
        <h2>Recommended Room Types</h2>
        <p style="padding: 0px 50px 0px 50px;">Offering striking views of the Indian Ocean, Beira Lake, and the city beyond, our 500 guest rooms and suites, and 41 serviced apartments are tastefully furnished to complement the urban-oceanside location and are among the largest in Colombo.</p>
      </div>
      
      <div class="card-list">
      <ul class="card-list-items">
        <li v-for="(item, index) in listItems" :key="index">
          <Card :item="item" />
        </li>
      </ul>
    </div>
      
      <Footer/>
    </div>
  </template>
  
<script>

import Footer from "./Footer.vue"
import Navbar from "./Navbar.vue";
import Card from "./Card.vue";
import singleRoomImage from "../assets/1.jpg";
import doubleRoomImage from "../assets/2.jpg";
import tripleRoomImage from "../assets/3.jpg";
import quadRoomImage from "../assets/4.jpg";
import octaRoomImage from "../assets/5.jpg";
  export default {
    components: {
    Navbar,
    Footer, // Register the Navbar component
    Card,
  },
  data() {
    return {
      listItems: [
        {
          title: "Single",
          description: "A room assigned to one person.",
          imageUrl: singleRoomImage, // Replace with the path to your image
        },
        {
          title: "Double",
          description: "A room assigned to two people.",
          imageUrl: doubleRoomImage, // Replace with the path to your image
        },
        {
          title: "Triple",
          description: "A room assigned to three people.",
          imageUrl: tripleRoomImage, // Replace with the path to your image
        },
        {
          title: "Quad",
          description: "A room assigned to four people.",
          imageUrl: quadRoomImage, // Replace with the path to your image
        },
        {
          title: "Hexa",
          description: "A room assigned to six people.",
          imageUrl: octaRoomImage, // Replace with the path to your image
        },
      ],
    };
  },
  };
  </script>
  
  <style scoped>
.appBodyCover {
  position: relative;
}

.appBodyCover img {
  width: 100%;
  height: 700px;
  background-size: 100% 100%;
  opacity: 0.4;
  z-index: -1;
}

.quote {
  text-align: center;
  position: absolute;
  top: 40%;
  width: 80%;
  padding-left: 180px;
  color: rgb(59, 59, 59);
}

.quote h1 {
  font-weight: 600;
  font-size: 40px;
}

.quote h3 {
  font-weight: 500;
  font-size: 20px;
}

.horizantalLine {
  margin: 50px;
}

.sectionTwo {
  text-align: justify;
}

.sectionTwo h2 {
  color: #777;
  font-weight: 400;
  padding-left: 30px;
}

.sectionTwo h3 {
  font-weight: 300;
  padding-left: 10px;
}

.list {
  color: #777;
  font-weight: 400;
  padding: 10px;
  display: flex; /* Use flexbox to display cards in a row */
  flex-wrap: wrap; /* Wrap cards to the next line if necessary */
  justify-content: center; /* Center cards horizontally */
}

.list li {
  padding: 10px;
  border-radius: 10px;
  margin: 10px; /* Add margin to separate cards */
  width: 200px; /* Set a fixed width for each card */
  box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.2);
  background-color: #fff;
  transition: transform 0.2s ease-in-out;
}

.list li:hover {
  background-color: antiquewhite;
  cursor: pointer;
  transform: scale(1.05); /* Enlarge card on hover */
}
.card-list {
  display: flex; /* Display cards horizontally */
  flex-wrap: wrap; /* Wrap cards to the next line if necessary */
  justify-content: center; /* Center cards horizontally */
  list-style: none; /* Remove bullets */
  padding: 0; /* Remove default padding for the ul element */
}
.card-list ul {
  list-style-type: none; /* Remove bullets for this specific <ul> */
  padding: 0; /* Remove default padding for the <ul> */
}

.card-list-items {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  padding: 0;
}
</style>

  