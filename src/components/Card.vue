<template>
    <div class="card">
      <div class="card-image">
        <img :src="item.imageUrl" alt="Room" />
      </div>
      <div class="card-content">
        <h2>{{ item.title }}</h2>
        <p>{{ item.description }}</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      item: Object, // Receive the item object from the parent component
    },
  };
  </script>
  
  <style scoped>
  /* Add your CSS styles for the card here */
  .card {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    padding: 20px;
    width: 200px; /* Set a fixed width for each card */
    border-radius: 10px;
    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.2);
    background-color: #fff;
    transition: transform 0.2s ease-in-out;
    margin: 10px; /* Add margin to separate cards */
  }
  
  .card-image img {
    max-width: 100%;
    height: auto;
  }
  
  .card:hover {
    background-color: antiquewhite;
    cursor: pointer;
    transform: scale(1.05); /* Enlarge card on hover */
  }
  </style>
  