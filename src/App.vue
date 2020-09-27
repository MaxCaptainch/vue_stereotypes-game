<template>
  <div id="app">
    <h1>Стереотипи</h1>
    <hr>
    <router-view/>
  </div>
</template>

<style scoped>

#app{
   text-align: center;
   color:#353635;
}
#app h1 {
  font-family: 'Roboto Slab', serif;
  font-size: 3em;
  font-weight: 700;
  line-height: 1.3;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #3d4449;
  margin:.5rem;
}

hr{
  border:2px solid #f56a6a;
  width: 90%;
}

@font-face {
  font-family: 'Roboto Slab';
  src: local('Roboto_Slab'), local('Roboto_Slab'),
    url('~@/assets/fonts/Roboto_Slab/RobotoSlab-VariableFont_wght.ttf') format( 'ttf')
}

</style>
