<template>

  <nav class="navBar">
        <div class="branding">
          My Blog

      </div>
      <ul class="nav-links">
      <input type="checkbox" id="checkbox_toggle"/>
      <label for="checkbox_toggle" class="hamburger">&#9776;</label>
      <div class="menu">

          <li><nuxt-link class="link" to="/">Home</nuxt-link></li>
           <li><nuxt-link class="link" to="/about">About</nuxt-link></li>

      </div>
      </ul>
  </nav>

</template>

<script>
export default{
    data(){
      return{

      }
    },
}
</script>

<style>
*{
    margin:0;
    padding: 0;
    box-sizing: border-box;
}
li{
    list-style: none;
}
.navBar{
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 5px;
    background-color: teal;
    position: fixed;
    left:0;           /* top left corner should start at leftmost spot */
  top:0;            /* top left corner should start at topmost spot */
  width:100vw;      /* take up the full browser width */
  z-index:200;  /* high z index so other content scrolls underneath */
  height:50px;
}
.nav-links .a{
    color: rgb(0, 0, 0);
}
.logo{
    font-size: 32px;
}
.branding{
    padding: 20px;
}

.menu{
display: flex;
gap: 1em;
font-size: 18px;
margin: 20px 20px;
}
.menu li:hover{
    background-color: rgb(0, 0, 0);
    border-radius: 5px;
    transition: 0.3s ease;
}
.menu li{
    padding: 2px 14px;
}

input[type=checkbox]{
    display:none;
}
.hamburger{
    display:none;
    font-size:24px;
    user-select:none;
}

@media(max-width:768px){
    .menu{
        display: none;
        position: absolute;
        background-color: black;
        right: 0;
        left: 0;
        text-align: center;
        padding: 16px 0;
    }
    .menu li:hover{
        display: inline-block;
        background-color: black;
        transition: .3s ease;
    }
    .menu li + li{
        margin-top: 12px;
    }
    input[type=checkbox]:checked ~ .menu{
        display: block;
    }
    .hamburger{
        display: block;
        margin-right: 10px;
        font-size: 25px;
    }
}
</style>
