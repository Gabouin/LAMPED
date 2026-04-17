# LAMPED - A SIMPLE LIGHT CONTROL MECHANISM

<img width="803" height="448" alt="image" src="https://github.com/user-attachments/assets/79f0fd06-d780-490f-a6a7-fe14eaa620d1" />

<br> 
<br>

This project was made for _RESOLUTION - WEEK 4_ and is basically 10 LEDs that shine in order (regulated by an LM3914) thanks to a potentiometer. 
<br>  
It's a visual experience designed to look like a small lamp, using the logic of the LM3914 driver to control an array of LEDs via a potentiometer. It’s perfect for a desk ornament, offering a fun, interactive lighting effect.
<br>   

## FEATURES
The board does:

**Interactive Light Control** : The small potentiometer allows you to sequentially activate the 10 LEDs, making the "lamp" brighter or dimmer.

**Cool Aesthetics** : The LEDs are arranged in a circular pattern to mimic the look of a traditional light bulb, giving it a unique visual style.

**USB Powered** : It plugs into any standard 5V USB port, making it easy to power at your desk or workstation. You could even create a small 3d print base where you plug this PCB and so you can have a small desk lamp !

## SCHEMATIC

I found a video on [youtube](https://www.youtube.com/shorts/ahxGdakDI9g) of the project I wanted to do and found the **good wiring diagram** to make it : 
<br>  
<br>  
<img width="338" height="371" alt="Capture d&#39;écran 2026-04-15 152251" src="https://github.com/user-attachments/assets/b07091f9-7281-42e1-9b71-18b77746e0a5" />
<br>  
<br>  
<br>  

I took inspiration from it and made **my schematic** on KiCad : 
<br>  
<img width="1108" height="773" alt="image" src="https://github.com/user-attachments/assets/50ad7688-248e-4473-be07-e0f020c6c042" />

## PCB

<img width="330" height="420" alt="image" src="https://github.com/user-attachments/assets/89e7096e-645f-4b43-b2e2-fd16c4cf1e40" /> <img width="370" height="420" alt="Capture d&#39;écran 2026-04-17 191458" src="https://github.com/user-attachments/assets/92893ec3-58d0-4f10-ac41-464cc5cfe0e1" />  


> The traces are like that on purpose to free the space in the middle !

## ASSEMBLY

**LED Placement** : The circular LED array defines the look. Align all 10 LEDs with the correct polarity (Cathode to the IC pins) to ensure they all work.

**Component Height** : Start with the lower components like resistors and the IC socket before soldering the LEDs, potentiometer, and USB connector.

**USB Connector** : Place the USB-A connector on the bottom edge of the board so it can plug in easily.

## USAGE

Connect the LAMPED board to a 5V USB power source (computer port or adapter).

Turn the small potentiometer to see the LEDs light up sequentially, increasing or decreasing the overall brightness.

## BOM  

<img width="843" height="349" alt="image" src="https://github.com/user-attachments/assets/99dd9157-e6fd-462e-817b-b13deed71f12" />

