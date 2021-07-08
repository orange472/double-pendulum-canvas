<!--author@ TonyLi-->
<!--projectname@ UTSA Visual Mathematics Research Group | Pendulum Simulation-->
<html>

<h1>Double Pendulum</h1>

<span>
    <label>Angle 1:</label>
    <input id="angle1Slider" class = "p1_slider" type = "range" min = "-90" max = "90">
</span>

<span>
    <label>Angle 2:</label>
    <input id = "angle2Slider" class = "p2_slider" type = "range" min = "-90" max = "90">
</span>

<br>

<span>
    <label>Length 1:</label>
    <input id="length1Slider" class = "p1_slider" type = "range" min = "50" max = "150">
</span>

<span>
    <label>Length 2:</label>
    <input id="length2Slider" class = "p2_slider" type = "range" min = "50" max = "100">
</span>

<br>

<span style="margin-bottom: 10px;">
    <label>Gravity:</label>
    <input id="gravitySlider" type = "range" min = "1" max = "19">
</span>

<span style="margin-bottom: 10px;">
    <label>Damping:</label>
    <input id="dampingCheckBox" type = "checkbox">
</span>

<br>

<canvas id="pCanvas" width="600" height="400"></canvas> 

<br>

<button id="startButton" type = "button" class = "start">Start</button>
<button id="resetButton" type = "button" class = "reset">Reset</button>

<script>
    var pCanvas = document.getElementById("pCanvas");
    var canvas = pCanvas.getContext("2d");
    canvas.translate(300, 100);

    var angle1Slider = document.getElementById("angle1Slider");
    var length1Slider = document.getElementById("length1Slider");
    var angle2Slider = document.getElementById("angle2Slider");
    var length2Slider = document.getElementById("length2Slider");

    //draw position on screen load
    drawPendulum(angle1Slider.value * Math.PI / 180, length1Slider.value, angle2Slider.value * Math.PI / 180, length2Slider.value);

    //draw initial position with user inputs
    angle1Slider.oninput = function() {
        drawPendulum(angle1Slider.value * Math.PI / 180, length1Slider.value, angle2Slider.value * Math.PI / 180, length2Slider.value);
    }

    length1Slider.oninput = function() {
        drawPendulum(angle1Slider.value * Math.PI / 180, length1Slider.value, angle2Slider.value * Math.PI / 180, length2Slider.value);
    }
    
    angle2Slider.oninput = function() {
        drawPendulum(angle1Slider.value * Math.PI / 180, length1Slider.value, angle2Slider.value * Math.PI / 180, length2Slider.value);
    }

    length2Slider.oninput = function() {
        drawPendulum(angle1Slider.value * Math.PI / 180, length1Slider.value, angle2Slider.value * Math.PI / 180, length2Slider.value);
    }

    //run simulation on start-button click
    startButton.onclick = function() {
        var angle1 = angle1Slider.value * (Math.PI / 180);
        var angle2 = angle2Slider.value * (Math.PI / 180);
        var angle1_v = 0;
        var angle1_a = 0;
        var angle2_v = 0;
        var angle2_a = 0;
        var m1 = 10;
        var m2 = 10;
        var g = gravitySlider.value;
        var t = 0;
        var interval = null;

        interval = setInterval(update, 1);
        document.getElementById("startButton").disabled = true;
        document.getElementById("resetButton").disabled = false;
        document.getElementById("angle1Slider").disabled = true;
        document.getElementById("angle2Slider").disabled = true;
        document.getElementById("length1Slider").disabled = true;
        document.getElementById("length2Slider").disabled = true;
        document.getElementById("gravitySlider").disabled = true;

        resetButton.onclick = function() {
            document.getElementById("startButton").disabled = false;
            document.getElementById("resetButton").disabled = true;
            document.getElementById("angle1Slider").disabled = false;
            document.getElementById("angle2Slider").disabled = false;
            document.getElementById("length1Slider").disabled = false;
            document.getElementById("length2Slider").disabled = false;
            document.getElementById("gravitySlider").disabled = false;

            clearInterval(interval);
            drawPendulum(angle1Slider.value * (Math.PI / 180), length1Slider.value, angle2Slider.value * (Math.PI / 180), length2Slider.value);
        }

        //calculate angular acceleration, which increments angular velocity, which then increments angular displacement
        function update() {
            angle1_a = calculate_angle1_a(angle1, length1Slider.value, angle2, length2Slider.value, angle1_v, angle2_v) / 1000;
            angle2_a = calculate_angle2_a(angle1, length1Slider.value, angle2, length2Slider.value, angle1_v, angle2_v) / 1000;
            angle1_v += angle1_a;
            angle2_v += angle2_a;
            angle1 += angle1_v;
            angle2 += angle2_v;

            //if an angle reaches 360 degrees/2pi radians, reset its value to 0 so that the text boxes in the upper-right corner don't show huge values
            if (Math.abs(angle1) >= 2 * Math.PI) {
                angle1 = 0;
            }

            if (Math.abs(angle2) >= 2 * Math.PI) {
                angle2 = 0;
            }

            if(document.getElementById("dampingCheckBox").checked) {
                angle1_v *= 0.998;
                angle2_v *= 0.998;
                t += 0.001;
            }

            drawPendulum(angle1, length1Slider.value, angle2, length2Slider.value);

            return t;
        }

        function calculate_angle1_a(angle1, L1, angle2, L2, angle1_v, angle2_v) {
            num1 = -1 * g * (2 * m1 + m2) * Math.sin(angle1);
            num2 = -1 * m2 * g * Math.sin(angle1 - 2 * angle2);
            num3 = -2 * Math.sin(angle1 - angle2) * m2 * (Math.pow(angle2_v, 2) * L2 + Math.pow(angle1_v, 2) * L1 * Math.cos(angle1 - angle2));
            den1 = L1 * (2 * m1 + m2 - m2 * Math.cos(2 * angle1 - 2 * angle2));

            angle1_a = (num1 + num2 + num3) / (den1);

            return angle1_a;
        }

        function calculate_angle2_a(angle1, L1, angle2, L2, angle1_v, angle2_v) {
            num1 = 2 * Math.sin(angle1 - angle2);
            num2 = (Math.pow(angle1_v, 2) * L1 * (m1 + m2));
            num3 = g * (m1 + m2) * Math.cos(angle1);
            num4 = Math.pow(angle2_v, 2) * L2 * m2 * Math.cos(angle1 - angle2);
            den1 = L2 * (2 * m1 + m2 - m2 * Math.cos(2 * angle1 - 2 * angle2));

            angle2_a = (num1 * (num2 + num3 + num4)) / (den1);

            return angle2_a;
        }
    }

    function drawPendulum(angle1, L1, angle2, L2) {
        var x = L1 * Math.sin(angle1);
        var y = L1 * Math.cos(angle1);
        var x2 = L2 * Math.sin(angle2);
        var y2 = L2 * Math.cos(angle2);
        
        canvas.translate(-300, -100);
        canvas.clearRect(0, 0, pCanvas.width, pCanvas.height);
        canvas.translate(300, 100);

        canvas.beginPath(); //rope for Pendulum 2
        canvas.save();
        canvas.lineWidth = 2.5;
        canvas.moveTo(x + x2, y + y2);
        canvas.lineTo(x, y);
        canvas.closePath();
        canvas.strokeStyle = "#4d2600";
        canvas.stroke();
        canvas.restore();

        //Pendulum 1
        canvas.beginPath(); //dashed line
        canvas.save();
        canvas.lineWidth = 1.5;
        canvas.setLineDash([4, 5]);
        canvas.moveTo(0, L1);
        canvas.lineTo(0, 0)
        canvas.closePath();
        canvas.strokeStyle = "#ffffff";
        canvas.stroke();
        canvas.restore();

        canvas.beginPath(); //rope
        canvas.save();
        canvas.lineWidth = 3;
        canvas.moveTo(x, y);
        canvas.lineTo(0, 0);
        canvas.closePath();
        canvas.strokeStyle = '#994d00';
        canvas.stroke();   
        canvas.restore();

        canvas.beginPath(); //ball
        canvas.save();
        canvas.arc(x, y, 15, 0, 2 * Math.PI);
        canvas.fillStyle = "#e6f2ff";
        canvas.fill();
        canvas.closePath();
        canvas.restore();

        canvas.beginPath(); //pivot point
        canvas.save();
        canvas.arc(0, 0, 3, 0, 2 * Math.PI);
        canvas.fillStyle = "#000000";
        canvas.fill();
        canvas.closePath();
        canvas.restore();

        //Pendulum 2
        canvas.beginPath(); //ball
        canvas.save();
        canvas.arc(x + x2, y + y2, 15, 0, 2 * Math.PI);
        canvas.fillStyle = "#fff2e6";
        canvas.fill();
        canvas.closePath();
        canvas.restore();

        canvas.font = "13px Arial"; //values
        canvas.fillStyle = "#ffffff";
        canvas.textAlign = "center";
        canvas.fillText("Angle 1: " + Math.round(angle1 * (180 / Math.PI)) + " degrees", 225, -70);
        canvas.fillText("Angle 2: " + Math.round(angle2 * (180 / Math.PI)) + " degrees", 225, -50);
    }
</script>

<style>
    @import url('https://fonts.googleapis.com/css2?family=Antonio&family=Quicksand:wght@500&display=swap');
    @import url('https://fonts.googleapis.com/css2?family=Antonio&family=Oxygen&family=Quicksand:wght@500&display=swap');

    button { 
        background-color: white;
        color: black;
        border-color: black;
        border-radius: 6px;
        border-width: 2px;
        width: 298px;
        padding: 6px 16px;
        margin-right: 3px;
        margin-top: 3px;
        text-align: center;
        font-size: 20px;
        font-family: 'Antonio', sans-serif;
        font-family: 'Quicksand', sans-serif;
    }

    button:hover {
        background-color: #0075ff;
        color: white;
        border-color: white;
        border-width: 2px;
    }

    button:disabled {
        background-color: #cbcbcb;
        color: white;
        border: none;
        border-color: white;
        box-shadow: 5px 5px 3px inset gray, -2px -2px 2px inset #d8d8d8;
        transform: translate(0, -20);
    }
    
    input[type = checkbox]:hover {
        background-color: #cbcbcb;
    }

    h1 {
        font-family: 'Antonio', sans-serif;
        font-family: 'Oxygen', sans-serif;
        font-family: 'Quicksand', sans-serif;
    }

    input[type = range] {
        width: 150px;
        margin-right: 5px;
    }

    input[type = checkbox] {
        margin-bottom: 6px;
    }
    
    label {
        float: left;
        margin-right: 5px;
        width: 70px;
        font-family: 'Antonio', sans-serif;
        font-family: 'Quicksand', sans-serif;
    }

    span {
        display: inline-block;
        overflow: hidden;
        padding: 0px 4px 0px 6px;
    }

    #pCanvas {
        background-color:#003366;
        border: 2px solid black;
        border-radius: 6px;
    }
</style>

</html>
