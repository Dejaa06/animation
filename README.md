<!DOCTYPE html>
<html>
    <head>
        <meta="UTF-8">
        <title>Animation</title>
    </head>
    <body>
        <div class="whell">
            <span class="line"></span>
            <span class="line"></span>
            <span class="line"></span>
            <span class="line"></span>
            <span class="line"></span>
            <span class="line"></span>
            <div class="cabin"></div>
            <div class="cabin"></div>
            <div class="cabin"></div>
            <div class="cabin"></div>
            <div class="cabin"></div>
            <div class="cabin"></div>
        </div>








    <style>
        .whell {
            border:  2px solid black;
            margin-left: 50px;
            border-radius: 50%;
            position: absolute;
            height: 55vw;
            width: 55vw;
            max-width: 500px;
            max-height: 500px;
            animation-name: wheel;
            animation-duration: 10s;
            animation-iteration-count: infinite;
            animation-timing-function: linear;
        }

        .line {
            background-color: black;
            width: 50%;
            height: 2px;
            position: absolute;
            left: 50%;
            top: 50%;
            transform-origin: 0% 0%;
            
        }

        .line:nth-of-type(2) {
            transform: rotate(60deg);
        }

        .line:nth-of-type(3) {
            transform: rotate(120deg);
        }

        .line:nth-of-type(4) {
            transform: rotate(180deg);
        }

        .line:nth-of-type(5) {
            transform: rotate(240deg);
        }

        .line:nth-of-type(6) {
            transform: rotate(300deg);
        }


        .cabin {
             background-color: red;
             width: 20%;
             height: 20%;
             position: absolute;
             border: 2px solid;      
             transform-origin: 50% 0%;
             animation: cabins 10s ease-in-out infinite;
        }

        .cabin:nth-of-type(1) {
             right: -8.5%;
             top: 50%;
        }

        .cabin:nth-of-type(2) {
             right: 17%;
             top: 93.5%;
        }

        .cabin:nth-of-type(3) {
             right: 67%;
             top: 93.5%;
        }

        .cabin:nth-of-type(4) {
             left: -8.5%;
             top: 50%;
        }

        .cabin:nth-of-type(5) {
             left: 17%;
             top: 7%;
        }

        .cabin:nth-of-type(6) {
             right: 17%;
             top: 7%;
        }

        @keyframes wheel {
            0% {
                transform: rotate(0deg);

            }

            100% {
                transform: rotate(360deg);

            }
        }

        @keyframes cabins {
            0% {
                transform: rotate(0deg); 

            }

            25% {
                background-color: yellow; 

            }

            50% {
                background-color: purple;

            }

            100% {
                transform: rotate(-360deg);

            }

        }
    </style>
    </body>
</html>
