.. include:: sub.txt

===============================
 animate_deformedshape command
===============================

.. function:: vfo.animate_deformedshape(model="ModelName",loadcase="LoadCaseName",scale=10,speedup=1,
										contour="none",setview="3D",line_width=1,node_for_th=None,node_dof=1,
										moviename=None,gifname=None)
	


   Displays an animation of the deformed structure by reading data from a saved output database. 
   The animation object should be stored as an variable in order for the animation to run.
   
   When saving the animation as a GIF file or .mp4 movie, the on-screen animation window may seem flickering based on the computer hardware.


   ========================  ======================================================================================================================================================
   ``model``    |str|     		Name of the model to read data from output database, created with `createODB()` command.
   ``loadcase`` |str|     		Name of the subfolder with load case output data.
   ``scale``    |int|     		Scale factor for to display mode shape. (optional, default is 10)
   ``speedup``  |int|     		A factor to speedup the animation. (optional, The default is 1)
   ``setview``  |str|        	sets the camera view to predefined angles. Valid entries are "xy","yz","xz","3D", or a list with [x,y,z] unit vector. Default is "3D". (optional)
   ``contour``  |str|        	Contours of displacement in x, y, or z. Default is "none". (optional)
   ``line_width``  |float|      Line width of the rendered elements. (optional)
   ``node_for_th``  |int| 		Node ID to display displacement time-history. (optional)
   ``node_dof``  |int| 			Degree-of-freedom to display displacement time-history of node_for_th. Default is 1. (optional)
   ``moviename``  |str| 		Filename to save animation as a movie in .mp4 format. (optional)
   ``gifname``  |str| 		 	Filename to save animation as a movie in .gif format. (optional)
   ========================  ======================================================================================================================================================

   
Examples: 

.. image:: /_static/Animation_Archetype.gif

::

   ani = vfo.animate_deformedshape(model="3D_Building", loadcase="Dynamic_GM1")
   
The above command animates the deformedshape of structure by reading data from `3D_Building_ODB` with a sub-folder `Dynamic_GM1` at default time-step speed.

::

   ani = vfo.animate_deformedshape(model="3D_Building", loadcase="Dynamic_GM1", speedup=4, scale=50, gifname="Building_Dynamic")

The above command animates the deformedshape of structure by reading data from `3D_Building_ODB` with a sub-folder `Dynamic_GM1` at a speed 4x the default saved steps using a scale factor of 50. The animation movie will be saved as `Building_Dynamic.mp4` in the current folder.
