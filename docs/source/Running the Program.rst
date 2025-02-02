Running the Program
====================
    
**DO NOT** run the program until the **ENTIRE** section has been read. 

After you complete the stock setup, tool changes, and offsets, you are almost ready to run the program. But, there are a few thing's you'll need to do, as well as some best practices. 

First, you will have to load the program onto the CNC's USB device.


Load the Program onto the USB
------------------------------

1. Take the USB out of the CNC machine (located on the side of the control panel as seen below). 

.. figure:: ../_static/images/CPS1.JPG
   :figwidth: 400px
   :target: ../_static/images/CPA1.JPG

2. Once the USB is inserted into the computer, open your CAM setup and click ‘Post Process’ located under 'Toolpath'.

.. figure:: ../_static/images/PP1.JPEG
   :figwidth: 700px
   :target: ../_static/images/PP1.JPEG

a. Make sure to pick the correct machine configuration. This should be 'HAAS (pre-NGC)/haas'.
    
b. Make sure that under 'Program Settings', you select 'Preload tool' to be 'No'
    
c. Make sure the program is named as numbers (a unique 4 digits that does not already exist on the USB)
    
d. Save the program under the USB device.

.. figure:: ../_static/images/PP2.JPEG
   :figwidth: 700px
   :target: ../_static/images/PP2.JPEG

3. Bring the USB back to the CNC.


Navigating to the Program on the CNC
-------------------------------------

1. To locate the program, press 'List Program’ > USB (using the cursor) > ‘enter’.

2. Find the folder you put your program in using the cursor. When found, press ‘enter’. 

3. Find the program using the cursor. When found, press ‘select program.’

.. raw:: html

    <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; height: auto;">
        <iframe width="560" height="315" src="https://www.youtube.com/embed/UqoNt2KK0Vc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div margin-bottom: 2em> 
The above step should have opened your program in the 'MEMORY' tab. If it doesn't open 'Memory' automatically, you can manually do it by pressing the 'MEM' button. 


There are a number of important things that you should do before you run the program...

* Make sure it’s the right program: 
    * If you included a 'description' in your CAM setup, this should show up in the memory tab on the screen.
    * Every tool you set up should be listed at the beginning of the code.
* Make sure the coolant is set to turn on. This is the M8 command at the beginning of each operation.
* Graph the program to make sure it's looking right. To do this, make sure you’re in memory. If not, press ‘MEM.’ Next, press ‘setting/graph’ TWICE and then ‘cycle start.’ Watch to make sure the program graphs the correct toolpath. To exit the graph, press 'MEM' again.
* **IMPORTANT:** Make sure the 'Rapid' is set to 5%! This is to make sure that you’ll have time to stop if the tool is about to crash. 
* Point the manual coolant nozzle towards the tip of the tool.
* Make sure everything is removed from the table inside the CNC machine, and the door is closed.
* Press the RESET button 2 or 3 times just to make sure the program is reset to the beginning. 

Once you ensure that you have followed all the above steps and have done your tool offsets correctly, you can run the program.


Running the Program
-------------------

1. Press 'Start cycle'

* Keep your hand on the feed hold at all times! If something goes wrong, you must be able to hit that button asap!

* Make sure the automatic coolant nozzle is pointing at the tool. Each tool may require the nozzle to be moved. You can do this manually by pressing 'Feed hold' so you can see what you're doing and then 'Coolant up' or 'Coolant down' to move the nozzle into the correct orientaation. When you're done, press 'Cycle start' again. 

You can also adjust the coolant nozzle before you run the program so that you do not need to touch it during the program.

**EMERGENCY STOP BUTTON**
--------------------------

In the event of the machine crashing and an emergency stop is needed, there is a large red button.
To activate the emergency stop, simply press this button.

.. figure:: ../_static/images/ESTOP.jpg
   :figwidth: 700px
   :target: ../_static/images/ESTOP.jpg
   
Once you press this button, alarms are activated and the machine will not work until these alarms have been cleared.

To clear these alarms:

1. Twist the emergency stop button in the direction the arrows are pointing. 

2. Press the 'reset' button until all alarms have been cleared. 

.. raw:: html

    <div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; height: auto;">
        <iframe width="560" height="315" src="https://www.youtube.com/embed/XUquIkJInNY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div margin-bottom: 2em> 




