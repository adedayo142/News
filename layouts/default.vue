<template>
  <div>





        <Navbar/>
        <Nuxt />
        <Footer/>

  </div>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data () {
    return {
      // items: [
      //   {
      //     title: 'Home',
      //     icon: 'home',
      //     to: { name: 'index' }
      //   },
      //   {
      //     title: 'Inspire',
      //     icon: 'lightbulb',
      //     to: { name: 'inspire' }
      //   }
      // ]
    }
  }
}
</script>
<style>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: sans-serif;
}
body{
  background-color: #eee;
}
a{
  text-decoration: none;
}
p{
  margin-bottom: 15px;
}
p:last-of-type{
margin-bottom: 0px;
}
</style>
