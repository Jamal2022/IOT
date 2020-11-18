# Arm control panel design with arduino

We use javascript for connect with arduino by communication device (Ex:ESP) 

## We use function servo(angle) for connect with arduino by ESP 

### First take the value of angle for the servo [onmouseup="servo1(this.value)"]

    <p>محرك 1 :<input type="range" min="0" max="180" onmouseup="servo1(this.value)" /></p>
    

### Second connect with arduino by ESP : Add ip address for the esp for connect with this page

    TextVar = "IP_Address";
    ArduinoVar = "http://" + TextVar + ":80";

### Third sends "sr1" for the servo 1 then "angle" for the value of this servo 


    function servo1(angle) 
    
    {
    TextVar = "IP_Address";
    ArduinoVar = "http://" + TextVar + ":80";
    $.get( ArduinoVar, { "sr1": angle })    ;
    {Connection: close};
    }
  


