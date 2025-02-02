Creating the Buckling Study
===========================

Similar to our previous static study, we can create a buckling study using “New Study” and selecting the “Buckling Study” 
option in Advanced Simulation.
 
.. figure:: ../_static/images/CreatingtheBucklingStudy1.png
    :figwidth: 600px
    :target: ../_static/images/CreatingtheBucklingStudy1.png 
 
Next, re-apply all the previous fixtures and forces and creating/refining the mesh for the bracket as we did in the initial 
study (Note that when you reapply the force the nut split sketch that was created earlier is now a clickable face to apply 
the force to, so you do not need to make a new split). It should be noted while reapplying fixtures that the virtual wall 
cannot be applied; This is OK and will not affect the final results in the buckling study. Re-completing these steps and 
running the study will create an Amplitude plot in the results tab of the simulation tree which allows us to visually see 
where the model is expected to buckle. Applying the 200 lb force at the hole as we did in the stress study, we obtain the 
model plot shown below.
 
.. figure:: ../_static/images/CreatingtheBucklingStudy2.png
    :figwidth: 600px
    :target: ../_static/images/CreatingtheBucklingStudy2.png 
 
As seen in the image above, we can see the behavior of the bracket when exhibited the load of 200 lb. Additionally, we can 
also see from the plot description that there is a given load factor for this simulation.

.. figure:: ../_static/images/CreatingtheBucklingStudy3.png
    :figwidth: 600px
    :target: ../_static/images/CreatingtheBucklingStudy3png 
 
A load factor is a multiplier value that gets multiplied with the applied load value to give the load value that the bracket 
would fail at. Since the bracket is under a 200 lb load and the load factor is 1.2625, the bracket will fail at 1.2638 times 
more than 200 lb meaning that the bracket will fail at 200 x 1.2638 lb, or 252.5 lb. 

Interpreting Results
^^^^^^^^^^^^^^^^^^^^

While in the case of this bracket it is predicted to fail due to shear as opposed to buckling, it should be noted that there 
is still a considerable amount of twisting occurring due to the applied load. Given a model of a different geometry, a part 
may experience more deflection or bending due to applied loads which can lead to that part failing due to buckling. It is 
for this reason that compressive effects on a model be considered alongside tensile effects when determining the method of 
failure in a model. In the case of our example, the load factor also serves as the Factor of Safety, meaning that since the
buckling FoS of 1.2625 is greater than the static FoS of 0.22, the bracket is predicted to fail due to shear. 
 
 
