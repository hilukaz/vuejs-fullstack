<template>
    <div class="card">
      <div class="card-content">
        <div class="flex-start"></div>
        <h3 class="card-title">Nome:{{ name }}</h3>
        <p class="card-description">preço:{{ price }}</p>
        <p class="card-description">bar_code:{{ bar_code }}</p>
        <div class="card-footer">
        <button class="card-button" >delete</button>
      </div>
       
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'CardA',
    props: {
      name: {
        type: String,
      },
      bar_code: {
        type: String,
      },
      price: {
        type: String,
      },
    }
  }
  
  console.log()
  </script>
  
  <style scoped>
  .card {
    border: 1px solid #ccc;
    margin: 50px;
    max-width: 350px;
    background-color: #fff;
    box-shadow: 0px 2px 2px rgba(0, 0, 0, 0.1);
    font-family: Arial, sans-serif;
  }
  
  
  
  .card-content {
    padding: 10px;
    padding-right: 200px;
  }
  
  .card-title {
    margin: 10px 0;
    
    font-size: 1.2rem;
    display: flex;
    justify-content: flex-start;
  }
  
  .card-description {
    margin: 10px 0;
    font-size: 1rem;
    color: #777;
    display: flex;
    justify-content: flex-start;
  }
  
  .card-footer {
    display: flex;
    justify-content: flex-end;
    margin-top: 10px;
    
  }
  
  .card-button {
    background-color: #0077c2;
    color: #fff;
    border: none;
    padding: 10px 20px;
    border-radius: 4px;
    font-size: 1rem;
    cursor: pointer;
  }
  </style>
  