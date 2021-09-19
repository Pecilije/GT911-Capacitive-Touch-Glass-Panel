# GT911-Capacitive-Touch-Glass-Panel
Using cheap Chinese capacitive touch glass panel connected to Arduino Leonardo (or Uno, Mega etc.) and sending touch coordinates to PC. We can send up to five simultaneous touches  and move them around the panel.

Okay, what can we see here?
First, an Arduino Leonardo microcontroller with some protoboard connections, a 20x4 CLCD display and a GOODIX GT911 capacitive touch panel glass. The resolution of the panel is 1024x600 pixels and the active touch surface is 155x90mm. The panel is completely transparent. Communication between components is via the I2C bus.
Second, the firmware on the Arduino Leonardo is written in C ++ in the Microsoft Visual Studio Code PlatformIO and the program on the PC is written in C# as a WPF application in Microsoft Visual Studio Community 2019.
In the upper right corner on the form, the listbox will display the COM port to which the Arduino Leonardo is connected, and next to it, two buttons for opening and closing the port. Appropriate messages will be sent to the CLCD.
In the upper middle of the form, clicking on the pink button, the top textblock will display the message which microcontroller is connected to that port.
The following is more like cosmetics. In the upper left corner, in the text box, you can type some text and use the radio buttons to select in which row on the CLCD it will be displayed as well as its position in the row: from the left margin, centric or to the right margin.
After opening the port, the GT911 is ready for operation (initialized). By touching one to five points at the same time, on the WPF form, they are displayed in a colored circles in which the ordinal number they touched is written and below them their current X and Y coordinates, so you can play as much as you want :-).
You will notice that the surface of the circles on the shape changes. It depends on the deformation of your finger or the surface it has touched. Weaker pressure - smaller surface, stronger pressure - larger surface. (Be careful not to overload it and break the panel).
You can see the working example on https://youtu.be/t6X8YDWSYBg.
You can change the code as you wish.
The both apps works fine for me but I can't guarantee that it will work for you.
There is the picture of my touch panel and the schematics how I connected panel to Arduino Leonardo 32-bit and optionally to Arduino Mega 2560.
Have fun!
