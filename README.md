<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body style="  background-image:url(https://images.unsplash.com/photo-1475274047050-1d0c0975c63e?ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mjl8fG5pZ2h0fGVufDB8fDB8fA%3D%3D&ixlib=rb-1.2.1&w=1000&q=80);">

    <div class="light">
        <article id="lighthouse">
            <div class="lights">
              <div class="light-left"></div>
              <div class="light-right"></div>
            </div>
            <div class="roof"></div>
            <div class="building">
                <div class="main"></div>
                <div class="base"></div>
            </div>
            <div class="sand"></div>
          </article>
    </div>
    <style>
        @-webkit-keyframes lighthouse {
      0% {
        -webkit-transform: perspective(100px) rotateY(0deg);
      }
      100% {
        -webkit-transform: perspective(100px) rotateY(360deg);
      }
    }
    @keyframes lighthouse {
      0% {
        -webkit-transform: perspective(100px) rotateY(0deg);
      }
      100% {
        -webkit-transform: perspective(100px) rotateY(360deg);
      }
    }
    @-webkit-keyframes shine {
      0% {
        opacity: 0;
      }
      25% {
        opacity: 0.1;
      }
      50% {
        opacity: 1;
      }
      75% {
        opacity: 0.1;
      }
      100% {
        opacity: 0;
      }
    }
    @keyframes shine {
      0% {
        opacity: 0;
      }
      25% {
        opacity: 0.1;
      }
      50% {
        opacity: 1;
      }
      75% {
        opacity: 0.1;
      }
      100% {
        opacity: 0;
      }
    }
    .light {
      margin: 0;
      margin-top: 15pc;
      display: flex;
      align-items: center;
      justify-content: center;
      background-color: transparent;
    }
    
    #lighthouse {
      width: 100%;
      max-width: 1400px;
      min-width: 300px;
      height: 400px;
      position: relative;
      background-color: #f5f5f5;
      border-radius: 10px;
      background-color: transparent;
      perspective: 700px;
      border: 10px solid black
      
    }
    #lighthouse .sand {
      width: 100%;
      height: 10%;
      position: absolute;
      bottom: 0;
      background-color: #f4e0d5;
      z-index: 3;
    }
    #lighthouse .sea {
      width: 100%;
      height: 25%;
      position: absolute;
      bottom: 0;
      background-color: #429abc;
    }
    #lighthouse .building {
      width: 60px;
      height: 60%;
      position: absolute;
      bottom: 20%;
      left: calc(50% - 30px);
      z-index: 1;
    }
    #lighthouse .base {
      width: 120px;
      height: 5%;
      position: absolute;
      left: -30px;
      bottom: -40px;
      background-color: #5a5a5a;
      border-radius: 20px 20px 0 0;
    }
    #lighthouse .base:after {
      content: "";
      width: 1.2em;
      height: 2.3em;
      position: absolute;
      left: calc(50% - 0.6em);
      bottom: 50%;
      background-color: #383838;
      border-radius: 50% 50% 0 0;
      box-shadow: 0 -60px 0 -5px #383838, 0 -100px 0 -5px #383838, 0 -140px 0 -5px #383838;
    }
    #lighthouse .main {
      width: 100%;
      height: 100%;
      background-image: repeating-linear-gradient(to top, #cf6766, #cf6766 1.25em, #fff 1.25em, #fff 3em);
      -webkit-transform: perspective(200px) rotateX(40deg);
    }
    #lighthouse .main:after {
      content: "";
      height: 100%;
      width: 50%;
      position: absolute;
      background-color: rgba(56, 56, 56, 0.3);
    }
    #lighthouse .roof {
      width: 60px;
      height: 15%;
      position: absolute;
      top: 20%;
      left: calc(50% - 30px);
      background-color: #858585;
      border-radius: 30% 30% 0 0;
      z-index: 9;
    }
    #lighthouse .roof:after {
      content: "";
      height: 100%;
      width: 50%;
      position: absolute;
      background-color: rgba(56, 56, 56, 0.3);
      border-radius: 50% 0 0 0;
    }
    #lighthouse .roof:before {
      content: "";
      width: 0.2em;
      height: 2em;
      position: absolute;
      left: calc(50% - 0.1em);
      bottom: 15%;
      background-color: #fdcf52;
      border-radius: 20%;
      box-shadow: -10px 0 0 #fdcf52, -20px 0 0 #fdcf52, 10px 0 0 #fdcf52, 20px 0 0 #fdcf52;
    }
    #lighthouse .lights {
      width: 400px;
      height: 40%;
      position: absolute;
      top: 10%;
      left: calc(50% - 200px);
      z-index: 8;
      -webkit-animation: lighthouse 10s linear infinite both;
              animation: lighthouse 10s linear infinite both;
    }
    #lighthouse .light-left {
      width: 70%;
      height: 40%;
      position: absolute;
      top: 23%;
      right: 35%;
      background-image: linear-gradient(to left, #fdcf52 40%, transparent);
      -webkit-transform: perspective(100px) rotateY(40deg);
    }
    #lighthouse .light-right {
      width: 70%;
      height: 40%;
      position: absolute;
      top: 23%;
      left: 35%;
      background-image: linear-gradient(to right, #fdcf52 40%, transparent);
      -webkit-transform: perspective(100px) rotateY(-40deg);
    }
    #lighthouse .overlay {
      width: 100%;
      height: 100%;
      position: absolute;
      background-color: #fdcf52;
      z-index: 10;
      opacity: 0;
      -webkit-animation: shine 5s linear infinite both;
              animation: shine 5s linear infinite both;
    }
    #lighthouse:after {
      content: "";
      width: 2px;
      height: 2px;
      position: absolute;
      top: 3%;
      left: 5%;
      border-radius: 50%;
      background-color: rgba(255, 255, 255, 0.5);
      box-shadow: 10px 10px white, 60px 10px rgba(255, 255, 255, 0.5), 40px 40px rgba(255, 255, 255, 0.5), 100px 15px rgba(255, 255, 255, 0.5), 30px 120px rgba(255, 255, 255, 0.5), 60px 10px 1px 1px rgba(255, 255, 255, 0.5), 200px 0px white, 220px 50px rgba(255, 255, 255, 0.5), 140px 30px 1px 1px rgba(255, 255, 255, 0.5), 10px 10px 2px 1px rgba(255, 255, 255, 0.5), 10px 10px rgba(255, 255, 255, 0.5), 250px 60px white, 300px 90px white, 250px 10px 1px 1px white, 350px 20px 1px 1px white, 320px 5px 1px 1px rgba(255, 255, 255, 0.6), 780px 10px white, 10px 960px rgba(255, 255, 255, 0.5), 840px 40px rgba(255, 255, 255, 0.5), 1405px 10px rgba(255, 255, 255, 0.5), 1020px 30px rgba(255, 255, 255, 0.5), 1040px 60px 1px 1px rgba(255, 255, 255, 0.5), 950px 27px white, 1150px 120px rgba(255, 255, 255, 0.5), 930px 140px 1px 1px rgba(255, 255, 255, 0.5), 1070px 10px 2px 1px rgba(255, 255, 255, 0.5), 1000px 10px rgba(255, 255, 255, 0.5), 860px 50px white, 990px 80px white, 1200px 150px 1px 1px white, 1220px 90px 1px 1px white, 1359px 60px 1px 1px rgba(255, 255, 255, 0.6);
    }
    </style>
    <div class="balloon">
        <img class="balloon" src="balloon.png">
    </div>
    <style>
        .balloon{
            width: 20%;
            height: 40%;
            position: fixed;
            top: 10% ;
            left: 10pc;
            animation: balloon 10s ease-in-out infinite ;
            overflow: hidden;

        }
        @keyframes balloon{
            0%,100%{
                left: 10%;
        
            }
            50%{
                left: 75%;
            }
            20%,40%,70%{
              top: 25%;
            }
            30%,60%,80%{
              top: 20%;
            }


        }
    </style>
    <div class="cloud">
        <img src="cloud.png" style="width: 20pc;position: fixed;top: 0;left: 0;opacity: 0.8;">
            <a style="width: 15pc;position: fixed;top: 4pc;left: 2pc;color: black;font-weight: 700;font-size: 1.6rem;z-index: 1;">
                Perfect Vision Board
            </a>
        <img src="cloud.png" style="width: 20pc;position: fixed;top: 0;left: 40pc;opacity: 0.3;">
        <img src="cloud.png" style="width: 20pc;position: fixed;top: 20pc;left: 20pc;opacity: 0.3;">
        <img src="cloud.png" style="width: 20pc;position: fixed;top: 10pc;left: 60pc;opacity: 0.3;">

    </div>
    
    <div id="balloon-container">
        <img src="kid.png" style="width: 10pc ;height: 10pc;background-color: transparent;position: absolute;top: 20%;animation: kid 15s ease-in-out infinite;
        ">
    </div>
    <style>
        @keyframes kid{
            0%,100%{
                left: 0%;
            }
            90%{
                left: 90%;
            }
            0%,30%,70%{
              top: 20%;
            }
            20%,40%,80%{
              top: 10%;
            }
        }
    </style>

    
</body>
</html>
