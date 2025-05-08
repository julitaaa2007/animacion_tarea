<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Luna con estrellas fugaces</title>
  <style>
    body {
      margin: 0;
      height: 100vh;
      background-image: url("https://img.freepik.com/vector-gratis/escena-paisaje-natural_1308-36982.jpg?semt=ais_hybrid&w=740");
      background-size: cover; 
      background-position: center;
      position: relative;
    }

    
    .luna {
      width: 200px;
      height: 200px;
      background-color: #f0e9d2;
      border-radius: 50%;
      position: absolute;
      top: 20px;
      right: 20px;
      z-index: 2;
      box-shadow:
        inset -8px -8px 0 rgba(0, 0, 0, 0.1),
        inset 5px 5px 0 rgba(255, 255, 255, 0.05),
        0 0 30px rgba(255, 255, 200, 0.3);
      opacity: 0; 
      animation: aparecerLuna 2s forwards;
    }


    @keyframes aparecerLuna {
      0% {
        opacity: 0;
        transform: scale(0.5);
      }
      100% {
        opacity: 1;
        transform: scale(1);
      }
    }
    p{
          color: rgb(96, 93, 93);
          font-size: 20px;
          position: absolute;
          top: 30%;
          left: 25%;
        
          
        }
      
    .estrella {
      position: absolute;
      width: 15px;
      height: 15px;
      background: white;
      border-radius: 50%;
      opacity: 0;
      pointer-events: none;
      z-index: 1;
      transition: opacity 0.3s ease;
      
    }
    

  
    #estrella1 {
      background: white;
      top: 10%; 
      left: 5%;
    }
    #estrella2 {
      background: rgb(255, 251, 0);
      top: 25%; 
      left: 10%;
    }
    #estrella3 {
      background: rgb(3, 248, 252);
      top: 40%;
      left: 15%;
    }
    #estrella4 {
      background: rgb(255, 47, 47);
      top: 60%; 
      left: 20%;
    }
    #estrella5 {
      background: rgb(149, 255, 2);
      top: 80%; 
      left: 25%;
    }
    #estrella6 {
      background: rgb(255, 255, 255);
      top: 50%; 
      left: 50%;
    }

    .estrella::after {
      content: '';
      position: absolute;
      width: 80px;
      height: 10px;
      background: linear-gradient(to right, white, transparent);
      top: 2px;
      left: 6px;
    }
    #estrella1::after {
      background: linear-gradient(to right, white, transparent);
    }
    #estrella2::after {
      background: linear-gradient(to right, rgb(255, 251, 0), transparent);
    }
    #estrella3::after {
      background: linear-gradient(to right, rgb(3, 248, 252), transparent);
    }
    #estrella4::after {
      background: linear-gradient(to right, rgb(255, 47, 47), transparent);
    }
    #estrella5::after {
      background: linear-gradient(to right, rgb(149, 255, 2), transparent);
    }
    #estrella6::after {
      background: linear-gradient(to right, rgb(255, 255, 255), transparent);
    }


    @keyframes estrellaFugaz {
      0% {
        transform: translateX(-20vw) translateY(-20vh);
        opacity: 0;
      }
      10% {
        opacity: 1;
      }
      100% {
        transform: translateX(120vw) translateY(120vh);
        opacity: 0;
      }
    }

    
    .luna:hover ~ #estrella1 {
      opacity: 1;
      animation: estrellaFugaz 4s forwards;
    }

    .luna:hover ~ #estrella2 {
      opacity: 1;
      animation: estrellaFugaz 5s forwards;
      animation-delay: 0.5s;
    }

    .luna:hover ~ #estrella3 {
      opacity: 1;
      animation: estrellaFugaz 3.5s forwards;
      animation-delay: 1s;
    }

    .luna:hover ~ #estrella4 {
      opacity: 1;
      animation: estrellaFugaz 4.5s forwards;
      animation-delay: 1.5s;
    }

    .luna:hover ~ #estrella5 {
      opacity: 1;
      animation: estrellaFugaz 4s forwards;
      animation-delay: 2s;
    }

    .luna:hover ~ #estrella6 {
      opacity: 1;
      animation: estrellaFugaz 4.5s forwards;
      animation-delay: 2.5s;
    }
    
  </style>
</head>
<body>
  <div class="luna"><p>TOCA AQUI</p></div>
  <div class="estrella" id="estrella1"></div>
  <div class="estrella" id="estrella2"></div>
  <div class="estrella" id="estrella3"></div>
  <div class="estrella" id="estrella4"></div>
  <div class="estrella" id="estrella5"></div>
  <div class="estrella" id="estrella6"></div>
</body>
</html>
