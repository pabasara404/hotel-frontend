<template>
    <Navbar/>
    <div class="appBodyAbout">
      <div class="details">
        <p>
          A personal tropical sanctuary that is perfect for escaping the city, Sunset Lodge Hotel, Colombo overlooks the Indian Ocean in the heart of the business district with direct access to the most extensive international shopping mall in Sri Lanka, Sunset Lodge’s own One Galle Face Mall. The hotel offers the finest accommodation in Colombo, an exciting new dining and social scene and the largest and extensive hotel conference and event facilities.
        </p>
        <p>Set on the Galle Face Promenade overlooking the Indian Ocean, this upmarket hotel is surrounded by high-end shopping and dining. It's a 6-minute walk from Galle Face Green urban park and 2 km from Beira Lake. Featuring city, lake, or ocean views, the refined rooms offer free Wi-Fi, flat-screen TVs, and tea and coffee-making facilities, plus minibars. Upgraded rooms add balconies. Suites offer separate living rooms and access to a club lounge.</p>
        <ul>
          <li>flat-screen TVs</li>
          <li>Suites offer separate living rooms</li>
          <li>541 rooms and suites</li>
          <li>Unrivalled shopping experience in Sri Lanka’s leading shopping mall</li>
          <li>access to a club lounge</li>
          <li>Sunset Lodge Cares: Our commitment to your well-being in our care</li>
        </ul>
        <br>
        <a href="#">Learn More</a>
      </div>
      <div class="photo">
        <img src="../assets/6.jpg" alt="">
      </div>
    </div>
  </template>
  
  <script>
  import Navbar from "./Navbar.vue";
  export default {
    components: {
    Navbar, // Register the Navbar component
  },
    data() {
      return {
        // You can add data properties here if needed
      };
    },
  };
  </script>
  
  <style scoped>
  .appBodyAbout{
  display: flex;
  
}

.details{
  margin:40px;
  padding: 20px;
  text-align: justify;
  border-radius: 10px;
  background-color: antiquewhite;
}
.details a{
  text-decoration: none;
  color: brown;
  padding: 10px;
  border: 1px solid brown;
  border-radius: 5px;
}
.details a:hover{
  background-color: rgb(216, 203, 186);
}
.photo img{
width: 650px;
height: 630px;
padding-right: 20px;
opacity: 0.7;}


  </style>
  