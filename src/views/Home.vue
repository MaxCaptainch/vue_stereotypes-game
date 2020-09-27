<template>
  <div class="home">
   <p>Більшість людей вважають стереотипи правильними, і виконують їх. Тут важливо розрізняти поняття правильності стереотипу і умовності . Але ж вигадані стереотипи часом керують колективною свідомістю.</p>
   <img src="@/assets/stereotypes.jpg" alt="">
   <p>Тому пропонуемо вам перевірити себе, за допомогою міні игри "Так/Ні</p>
   
   <router-link to="/questions">Почати</router-link>
  </div>
</template>

<script>
// @ is an alias to /src


export default {
  name: 'Home',
  components: {
    
  }
}
</script>

<style>

a {
  width: 75px;
  display: block;
  font-weight: bold;
  font-family: Roboto Slab,serif;
  color: #f56a6a!important;
  font-size: 80%;
  font-weight: 700;
  cursor: pointer;
  vertical-align: middle;
  letter-spacing: .075em;
  line-height: 3.5em;
  padding: 0 2.25em;
  text-align: center;
  text-decoration: none;
  text-transform: uppercase;
  white-space: nowrap;
  background-color: transparent;
  border-radius: .375em;
  border:2px solid #f56a6a;
  margin:0 auto; 
  margin-top: .5rem;
}



img {
  height: auto;
  width: 90%;
  max-width: 540px;
  margin: .5rem;
}

p{
	width: 90%;
	max-width: 90%;
	margin:0 auto; 
}
</style>