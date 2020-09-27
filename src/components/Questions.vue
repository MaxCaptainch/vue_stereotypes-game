<template>
  <div class="questions">
    <h2 :class = "{'hidden':hidden}" >{{stereotypes[index].title}}</h2>
    <h2 :class = "{'hidden':!hidden}" >Тепер ви можете перейти до результату!</h2>
    <img :class = "{'hidden':hidden}" :src="stereotypes[index].img"  alt="">
    <p :class = "{'hidden':hidden}">Як ви вважаєте це стереотип чи ні?</p>
    <button :class = "{'hidden':hidden}"class = "btn yes" v-on:click="userAnswer.push(true);showNext();" >Так</button>
    <button :class = "{'hidden':hidden}" class = "btn no" v-on:click="userAnswer.push(false);showNext();">Ні</button>
    <router-link :class = "{'hidden':!hidden}" to="/result" v-bind:stereotypes="stereotypes">Результат</router-link>
    
  </div>
</template>

<script>

export default{

	data(){
		return{
			stereotypes:[
				{	id: 1, 
					title: 'Люди з блакитними очима зявилися відносно не давно',
					feedback:'',
					img:require('@/assets/eyes.jpg'),
					fact: true,
				},
				{	id: 2,
					title: 'Кішки найпопулярніші тварини в інтернеті', 
					feedback:'',
					img:require('@/assets/catvsdog.jpg'),
					fact: false
				},
				{	id: 3, 
					title: 'У японців очі вужче ніж у європейців.', 
					feedback:'',
					img:require('@/assets/japanes.jpg'),
					fact: false
				},
				{	id: 4, 
					title: 'У чоловіків - мізки більше.', 
					feedback:'',
					img:require('@/assets/brains.jpg'),
					fact: true
				},
				{	id: 5, 
					title: 'Країна з найбільшою кількістю повних людей - Америка.',
					feedback:'', 
					img:require('@/assets/fatman.png'),
					fact: false
				}				
			],
			userAnswer:[],
			index:0,
			hidden: false
		}
	},
	components:{
		
	},
	methods:{
		showNext(){
			if (this.index == this.stereotypes.length-1){
				this.hidden = true; 
			}
			else{
				this.index+=1	
				
			}
		}
	}
	
}
</script>


<style scoped>
.btn{
	width: 100px;
	height: 50px;
	margin-top: 1rem;
	border:none;
  	font-size: 80%;
  	font-weight: 700;
  	cursor: pointer;
  	vertical-align: middle;
  	letter-spacing: .075em;
  	line-height: 2.5em;
  	text-align: center;
  	text-decoration: none;
  	text-transform: uppercase;
  	background:none;
  	margin: 0.5rem;
  	outline: none;
 }

.yes{
	border-right:1px solid #f56a6a;
	color: #f56a6a;
}

.no{
	border-left:1px solid #00d4ff;
	color:#00d4ff;
}
.yes:hover{
	background: linear-gradient(0.75turn, #f56a6a 75%, #fff);
	
	
	color:#fff;
	 
}

.no:hover{
	background: linear-gradient(0.25turn, #00d4ff 75%, #fff);
	
	color:#fff;
	 
}


.hidden{
	display: none;
}
</style>