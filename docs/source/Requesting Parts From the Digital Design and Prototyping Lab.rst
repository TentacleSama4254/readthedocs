Requesting Parts From The Digital Design and Prototyping Lab
============================================================

3D Printing Design Guide
------------------------

.. figure:: ../_static/images/3DPDG1.PNG
    :figwidth: 700px
    :target: ../_static/images/3DPDG1.PNG

Introduction
^^^^^^^^^^^^

3D printing or additive manufacturing is a process in which solid objects are made from a digital file. The
most widely used technic is Fused Deposition Modeling (FDM) in which material is layered to create
polymer-based parts, ranging from basic to complex geometrical shapes. These can be standalone parts
and/or components of a bigger structure. The relative speed of creating these parts (a couple of hours
depending on size, design, and infill) allows for proof of concepts to be developed rapidly, moving past 3D
modeling, a very powerful tool tied to 3D printing. The end results used to be used exclusively for
prototyping, however, due to the advancements of 3D printing technology and materials, 3D prints are
being used more frequently as end products and parts.

For more detailed information please visit the sources used under :ref:`Reference List`.

Materials
^^^^^^^^^

The most common materials for 3D printing are **Poly Lactic Acid (PLA)** and **Acrylonitrile Butadiene
Styrene (ABS)**. PLA filament is a biodegradable material that is easy to print due to its low heating
requirements, however it does not possess a very high resilience to UV rays, its more suitable for parts
used indoors and at around room temperature. ABS filament in the other hand requires a higher
temperature to be printed, but it offers UV resilience as well as better mechanical properties in high
temperature environments.

3D Printer
^^^^^^^^^^

At the Digital Design and Prototyping Lab (DDPL) we employ the use of Stratasys’ uPrint SE 3D printers.
These high end machines have an enclosed chamber that allow for even cooling of the 3D model as it is
printed, minimizing the issues of warping and delamination.
Keep in mind these **technical specifications** when creating a 3D model to be printed with the uPrint SE:

.. figure:: ../_static/images/3DPDG2.PNG
    :figwidth: 700px
    :target: ../_static/images/3DPDG2.PNG

Modelling
^^^^^^^^^

One of the advantages of 3D printing is that very complex models can be achieved. However, when
crafting your 3D model in a computer-aided design (CAD) software, such as SolidWorks, some design
considerations can help ensure better results.

**Resolution:** Similar to image resolution, a 3D printer has a minimum feature analogous to a pixel in 
picture, this is the smallest “dot” it can print, and it is dependent on the nozzle size.
Resolution is divided into XY-resolution, dependent on the nozzle diameter and the smallest movement the 
stepper motor on the printer can achieve and the Z-resolution is dependent on the layer height.
The uPrint SE at the DDLP can achieve a layer of 0.254 mm (.010 in.).

.. figure:: ../_static/images/3DPDG3.PNG
    :figwidth: 600px
    :target: ../_static/images/3DPDG3.PNG

.. figure:: ../_static/images/3DPDG4.PNG
    :figwidth: 600px
    :target: ../_static/images/3DPDG4.PNG

**Orientation:** Printing orientation of the 3D model can greatly
improve the surface quality of the print. The figure displays the same
3D model printed horizontally and vertically. The horizontally print
would display a “staircase” pattern, while the on vertically print this
patter would be greatly reduced achieving a smoother print.
Conversely, when printing parts that would undergo a mechanical
load, the former would support more force applied to it at the peak of
the semi-dome than the latter.

.. figure:: ../_static/images/3DPDG5.PNG
    :figwidth: 600px
    :target: ../_static/images/3DPDG5.PNG

**Size:** If you are making a display model, then this is less critical as you can scale your design before printing to be
within the boundaries of the printing volume. This is determined by the building platform’s area and the height of the
printing chamber. 203 x 203 x 152 mm (8 x 8 x 6 in).

**Wall thickness:** A minimum wall thickness is required for the
model to be able to print and be structurally sound. This dimension
would be affected if the model needs to support any force, but as a
rule of thumb for ABS it is recommended to use a minimum wall
thickness of 1.2mm.

**Shrinkage and Assembly:** When printing parts that are design to
be connected to each other, keep in mind the shrinkage that the
prints will undergo. This deviation of the print from the model’s
nominal size is also known as dimensional accuracy and is
generally around 0.1% or ±0.2mm.

.. figure:: ../_static/images/3DPDG6.PNG
    :figwidth: 800px
    :target: ../_static/images/3DPDG6.PNG

**Embossed and Engraved Details:** Engraving refers to details added into the print (inwards), a minimum line
thickness of 1 mm and a depth of 0.3 mm is recommended. By contrast, embossing are
details that protrude from the printed model, a line thickness of at minimum 2.5 mm and a
depth of at least 0.5 mm is advice. Engravings are usually preferred as they
require much lower tolerances than embossing details.

.. figure:: ../_static/images/3DPDG7.PNG
    :figwidth: 800px
    :target: ../_static/images/3DPDG7.PNG

**Support Material:** To be able to achieve intricate designs most 3D printers employ support material. 
The most popular ones being soluble and breakaway ones. Both types of supports have their cons and pros, soluble 
support materials are easy to remove, since it dissolve on a solution, leaving behind a clean print, however some
soluble support material such as PVA take up to 24hrs to fully dissolve. By contrast, breakaway support materials can
be removed from the print as soon as the model is completed, but in certain complex geometries they
tend to leave residue behind and/or are difficult to completely remove without damaging the print if the design 
possess deep channels or crevices in the inside faces of the model, especially if no exit hole is built into the design. 
This is very import to keep in mind when modeling your 3D design.

.. figure:: ../_static/images/3DPDG8.PNG
    :figwidth: 600px
    :target: ../_static/images/3DPDG8.PNG

.. figure:: ../_static/images/3DPDG9.PNG
    :figwidth: 600px
    :target: ../_static/images/3DPDG9.PNG

**Moving Parts:** Support material allows for the printing of preassembled models with moving parts, for these to print
successfully a minimum clearance of 0.4mm is advised, the greater the space that can be afford, the better chance
the model has to print properly.

.. figure:: ../_static/images/3DPDG10.PNG
    :figwidth: 700px
    :target: ../_static/images/3DPDG10.PNG

STL Format
^^^^^^^^^^

After you have finished your design, save the SolidWorks model in the native format SolidWorks Part File
(SLDPRT) as well as the Standard Triangle/Tessellation Language file format (STL) [1]. To save your
model in STL format go to File>>Save as, and change the file format from SolidWorks Part (.prt;.sldprt)
to STL (.stl) in the prompted window, as shown in the image below:

.. figure:: ../_static/images/3DPDG11.PNG
    :figwidth: 600px
    :target: ../_static/images/3DPDG11.PNG

The SLDPRT file stores the part as a solid model, keeping the specified details of material, color, and
texture. On the other hand, an STL file stores only the information of the 3D model surface, it represents
this surface as small adjacent triangles.

.. figure:: ../_static/images/3DPDG12.PNG
    :figwidth: 700px
    :target: ../_static/images/3DPDG12.PNG

Printing
^^^^^^^^

The .STL file will be imported into a slicer, a software that produces a path for the 3D printer to follow to
be able to print the model. This set of commands or language is known as G-code, and it tells the printer
what movements to make from begging to end of the print.

.. figure:: ../_static/images/3DPDG13.PNG
    :figwidth: 700px
    :target: ../_static/images/3DPDG13.PNG

Cost
^^^^

The cost of the 3D printed models is dependent on its final volume and material use to print it. At the SDH
the material of choice is ABS P430, with a cost of $7.50/in3. Small parts are usually a couple of cubic
inches in volume.

A final cost will be provided after the STL file of the model and the uPrint Confirmation Form is filled. For a
quick estimate, use the cost per inch and the volume of your model. This can be found in SolidWorks
under Evaluate >> Mass Properties >> Volume.

.. figure:: ../_static/images/3DPDG14.PNG
    :figwidth: 800px
    :target: ../_static/images/3DPDG14.PNG

Reference List
^^^^^^^^^^^^^^

Cthornsberry. (2019, May 1st). 3space. (3space) Retrieved November 27th, 2020, from
	https://3space.com/blog/what-does-resolution-mean-in-3d-printing/

SAS, D. (n.d.). Logiciel Cura by Dagoma | Dagoma. (Dagoma SAS) Retrieved November 1, 2020, 
	from https://www.dagoma3d.com/en_US/logiciel-cura-by-dagoma

SLDPRT to STL: How to Convert SLDPRT Files to STL | All3DP. (n.d.). (All3DP) 
	Retrieved November 1, 2020, from https://all3dp.com/2/sldprt-to-stl-how-to-convert-sldprt-files-to-stl/

STL to G-Code: How to Convert STL Files to G-Code | All3DP. (n.d.). (All3DP) Retrieved November 
	1, 2020, from https://all3dp.com/2/stl-to-g-code-how-to-convert-stl-files-to-g-code/

What is an STL file? (n.d.). (Sculpteo) Retrieved November 1, 2020, from 
	https://www.sculpteo.com/en/3d-learning-hub/create-3d-file/what-is-an-stl-file/


How to Request 3D Print
-----------------------

.. figure:: ../_static/images/3DPR1.png
    :figwidth: 700px
    :target: ../_static/images/3DPR1.png

1. Create your design in any computer-aided design (CAD) software and save it as an STL file. 

2. Fill out the Client Information on the :ref:`uPrint Confirmation Form` to obtain a cost 
   estimate. (*For modelling  parts 80% infill is recommended, if the part is meant to be used 
   mechanically, solid (100%) infill is  more appropriate*).

3. Send the filled form and attached STL file of your model to DDPL@mun.ca

4. A quote for the print would be issued, once this quote is received, proceed to the 
   Cashier’s  Office, and make the payment for your 3D print.

5. Take the request form and proof of payment to EN-1020.

6. Wait for your printing confirmation email and pick up your 3D printed part at EN-1017. 
   The usual  printing time is 3-5 business days. For a more accurate time estimates please 
   call 709-725-8201. *For more detailed information visit* :ref:`3D Printing Design Guide`.


uPrint Confirmation Form
------------------------

:download:`pdf <uPrint Confirmation Form.pdf>`















 



