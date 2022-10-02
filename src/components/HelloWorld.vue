<template>
  <div>
    <header class="t-center">
      <div id="box_logo">
        <img src="../assets/header/AppleLogo.svg" alt="logoNasa" id="logo">
      </div>
        <ul class="d-flex">
          <li class="text-green "> 
            <a href="#sobreElProyecto">
              Sobre el proyecto
            </a>
          </li>
          <li class="text-green ">
            <a href="#herramientas">
              Herramientas
            </a>
          </li>
          <li class="text-green ">
            <a href="#rueda">
              rueda
            </a>
          </li>
          <li class="text-green ">
            <a href="#recreación">
              recreación
            </a>
          </li>
          
        </ul>
    </header>
    <body>
      <div class="container">

        <div class="box-title">
          <h1 class="title text-green">WELCOME TO THE 'OUTFITTING A MARS HABITAT' CHALLENGE 🛸</h1>
        </div>

        <div class="box-title2">
          <a name="sobreElProyecto"></a>
          <h1 class="title text-white">DESIGNED BY: 🍎 APPLE FROM MARS...</h1>
        </div>

        <div id="about" class="m-t-10">
          <h2 class="text-green">Sobre el proyecto:</h2>
          <p class="t-center">
           Imagina que eres un astronauta recién llegado al Planeta Rojo.
            Su hábitat ha sido preconstruido para usted, pero, aparte de tres impresoras 3D, no tiene la mayoría de las cosas que necesita para vivir y trabajar.
            Su desafío es diseñar herramientas, muebles y otros elementos que lo ayuden en su misión de un año. Además, una rueda de su rover está dañada.
          </p>
        </div>

        <a name="herramientas"></a>
        <div class="m-t-10">
          <h1 class="text-green">Herramientas:</h1>
          <div class="box4tools">
            <div class="box4oneTool" v-for="(herramienta,idx) in listaHerramientas" :key="idx">
              <h2 class="text-green">
                {{herramienta.nombre}}
              </h2>
              <div class="slider-container">
                <div v-for="(currency, idx2) in herramienta.imagenes" :key="idx2">
                  <p>{{currency.descrip}}</p>
                  <img :src="currency.url" alt="herramienta3D" >
                </div>
              </div>
              <h3>
                {{herramienta.descripcion}}
              </h3>
            </div>                        
          </div>
        </div>
        
        <a name="rueda"></a>
        <div>
          <h1 class="text-green">Rueda del Rover:</h1>
          <div class="box4tools">
            <div class="box4oneTool" v-for="(herramienta,idx) in ROVER" :key="idx">
              <h2 class="text-green">
                {{herramienta.nombre}}
              </h2>
              <div class="slider-container">
                <div v-for="(currency, idx2) in herramienta.imagenes" :key="idx2">
                  <p>{{currency.descrip}}</p>
                  <img :src="currency.url" alt="herramienta3D" >
                </div>
              </div>
              <h3>
                {{herramienta.descripcion}}
              </h3>
            </div>
          </div>
        </div>

        <a name="recreación"></a>
        <div>
          <h1 class="text-green">Recreación:</h1>
          <div class="box4tools">
            <div class="box4oneTool" v-for="(herramienta,idx) in recreations" :key="idx">
              <h2 class="text-green">
                {{herramienta.nombre}}
              </h2>
              <div class="slider-container">
                <div v-for="(currency, idx2) in herramienta.imagenes" :key="idx2">
                  <p>{{currency.descrip}}</p>
                  <img :src="currency.url" alt="herramienta3D" >
                </div>
              </div>
              <h3>
                {{herramienta.descripcion}}
              </h3>
            </div>
          </div>
        </div>
      </div>
    </body>
  </div>
</template>

<script>  
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      
      recreations: [
        {
          nombre: 'Juegos recreativos',
          descripcion: '"El entretenimiento es fundamental para una buena salud mental." ',
          imagenes: [
            {descrip: 'Ping Pong Marciano',url:require("../assets/Herramientas/game1.jpeg")},
            {descrip: 'Red Ping Pong',url:require("../assets/Herramientas/game3.jpeg")},
            {descrip: 'TaTeTi espacial',url:require("../assets/Herramientas/game2.jpeg")}
          ]
        },
      ],

      ROVER: [
        {
          nombre: 'caterpillar wheel 🐛',
          descripcion: 'Rueda con un sistema de resortes de un material flexible, resistente a la tracción, elongación a rotura, alta resistencia química, contracción térmica baja y alta resistencia al corte.',
          imagenes: [
            {descrip: 'Sistema de amortiguacion',url:require("../assets/Herramientas/1rueda.jpeg")},
            {descrip: 'Modelo 3D',url:require("../assets/Herramientas/2rueda.jpg")},
            {descrip: 'Diseño completo',url:require("../assets/Herramientas/rueda3.jpg")}
          ]
        },
      ],

      listaHerramientas: [
        {
          nombre: 'Herramienta universal 🔧',
          descripcion: 'Mango con 2 encastres en ambos extremos que permite incrustar diferentes cabezales de herramientas y utensilios.',
          imagenes: [
            {descrip: 'Mango de frente',url:require("../assets/Herramientas/mango1.jpeg")},
            {descrip: 'Mango del revez',url:require("../assets/Herramientas/mango2.jpeg")},
            {descrip: 'Cabezales de herramientas',url:require("../assets/Herramientas/puntas.jpeg")},
            {descrip: 'Cabezales de utensilios',url:require("../assets/Herramientas/utensilios.jpeg")},
          ]
        },
      ],
      
    };
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

  * {
    line-height: 2;
    font-family: 'Silkscreen', cursive;
    transition-duration: 0.3s;
  }

  #about {
    background: #ffffff66;
    border: 1px solid;
    border-radius: 25px;
    padding: 2em;
  }

  #about:hover {
    -webkit-transform:scale(1.05);transform:scale(1.05);
  }

  .box-title {
    margin-top: 7em;
    width: min-content;
    display: flex;
    margin-left: 12%;
  }

  .box-title2 {
    margin-top: 2em;
    width: min-content;
    display: flex;
    margin-left: 27%;
  }

  .m-t-10 {    
    margin-top: 10em;
  }

  a {
    color:#20ff00;
    text-decoration: none;
  }

  a:link {text-decoration: none }

  a:visited {color:#20ff00; text-decoration: none }

  .container {
    margin-left: 5em;
    margin-right: 5em;
    padding-top: 2em;
  }

  .box4tools .box4oneTool:last-child {
    margin-bottom: 10em;
  }

  .box4tools {
    flex-wrap: wrap; 
    justify-content:center;
    display: flex;
  }

  .title {
  width: 0;
  overflow: hidden;
  white-space: nowrap;
  font-size: 2rem;
  margin: 0 auto;
  font-family: "Courier New";
  border-right: 0.15em solid #20ff00;
  animation: typing 4s steps(38) 1s 1 normal both, blink 1s steps(1) infinite;
  }
  @keyframes typing {
    from {
      width: 0;
    }
    to {
      width: 100%;
    }
  }
  @keyframes blink {
    50% {
      border-color: transparent;
    }
  }

  .box4oneTool {
    padding: 2em;
    max-width: 50%;
    background: #ffffff66;
    border:1px solid black; 
    margin-top: 2em;
    border-radius: 5px;
    min-width: 38em;
    text-align: center;
  }

  .box4oneTool:hover {
    -webkit-transform:scale(1.05);transform:scale(1.05);
  }

  .t-center {
    text-align: center;
  }

  .text-green {
    text-align: center;
    color: #20ff00;
    text-shadow:  2px 0 #000, -2px 0 #000, 0 2px #000, 0 -2px #000;
  }

  .text-white {
    text-align: center;
    color: #f2f2f2;
    text-shadow:  2px 0 #000, -2px 0 #000, 0 2px #000, 0 -2px #000;
  }

  body {
    margin: 0;
    margin-top: 85px;
    width: 100%;
    height: 100%;
    background: url("../assets/body/fondo.jpg");
    background-size: 100% 100%;
    
  }

  #box_logo {
    margin-left: 2em;
    display: flex;
  }
  .d-flex {
    display: flex;
  }

  ul {
    list-style: none;
    width: 50%;
    margin: 0;
    display: flex;
    justify-content: space-around;
    align-items: center;
  }

  li:hover {
    cursor: pointer;
    font-size: large;    
    background: #ffffff8a;
    padding: 5px;
    border-radius: 20px;

  }

  #logo {
    width: 80px
  }

  #logo:hover {
    -webkit-transform:scale(1.3);transform:scale(1.3);width: 80px
  }

  .slider-container {
    display: flex;
    width: 100%;
    overflow-x: scroll;

    scroll-snap-type: x mandatory;
    scrollbar-color: yellow #800080;
    scrollbar-width: 10px;
  }

  .slider-container img {
    /* max-height: 24em; */
    height: 20em;
    /* width: 20em; */
    /* min-height: 100%; */
    border-image: cover;
    /* object-fit: none; */
    scroll-snap-align: center;
  }

  header {
    top: 0;
    display: flex;
    min-width: 100%;
    position: fixed;
    z-index: 99;
    width: 100%;
    justify-content: space-between;
    text-align: center;
    height: 85px;
    border: none;
    background: #000 url("../assets/header/Fondo2.jpg");
    max-width: 1366px;
    color: white;
  }

</style>
