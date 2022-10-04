.. include:: sub.txt

============================
 plot_deformedshape command
============================

.. function:: vfo.plot_deformedshape(model="ModelName",loadcase="LoadCaseName",scale=10,tstep=-1,overlap="no",contour="none",setview="3D", contourlimits=None, filename=None)

   Displays the deformed shape of the structure by reading data from a saved output database.

   ==========================  ======================================================================================================================================================
   ``model``     |str|     		Name of the model to read data from output database, created with `createODB()` command.
   ``loadcase`` |str|      		Name of the subfolder with load case output data.
   ``scale``   |float|       	Scale factor for to display mode shape. (optional, default is 10)
   ``tstep``    |float|   		Approximate time of the analysis at which deformed shape is to be displaced. (optional, default is the last step)
   ``setview``  |str|        	sets the camera view to predefined angles. Valid entries are "xy","yz","xz","3D", or a list with [x,y,z] unit vector. Default is "3D". (optional)
   ``contour``  |str|        	Contours of displacement in x, y, or z. Default is "none". (optional)
   ``contourlimits``  |list| 	A list of minimum and maximum limits of the displacement contours. (optional)
   ``filename``  |str| 		 	Filename to save an image of the modeshape. (optional)
   ==========================  ======================================================================================================================================================


   
Examples: 
    
   ``vfo.plot_deformedshape(model="TwoSpan_Bridge", loadcase="Dynamic_GM1")``
                 Displays the deformedshape of structure by reading data from `TwoSpan_Bridge_ODB` with a sub-folder `Dynamic_GM1` at the last analysis step (default) with a default scale factor of 10.


   ``vfo.plot_deformedshape(model="TwoSpan_Bridge", loadcase="Dynamic_GM1", tstep=24.0, scale=50)``
                 Displays the deformedshape of structure by reading data from `TwoSpan_Bridge_ODB` with a sub-folder `Dynamic_GM1` at the analysis time closest to 24.0 sec with a scale factor of 50.


.. image:: /_static/Deformedshape_Archetype.png