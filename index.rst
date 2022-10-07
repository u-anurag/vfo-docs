.. include:: sub.txt

=========================
 vfo
=========================

IMPORTANT ANNOUNCEMENT: The plotting backend for vfo is being switched to a vtk based plotting tool PyVista starting vfo 0.0.6 for smooth interaction in large OpenSees model. Some of the commands are changing
and the older commands will not work with the new updated version. Please read this document carefully. 


vfo (Visualization for OpenSees) is a Python package to make your life better by helping you visualize your `OpenSees <https://openseespydoc.readthedocs.io/en/latest/index.html>`_ models, Python or Tcl. 
It utilizes `PyVista <https://docs.pyvista.org/index.html>`_ library to plot 2D and 3D models in a dedicated interactive window. You can use click-and-hold to change the view angle and zoom the plot. 
The model image can be saved with the desired orientation directly from the interactive plot window. 

**Animation**: To save the animation movie as .mp4 file, `FFmpeg <https://www.ffmpeg.org/about.html>`_ codecs are required.


Following elements are supported:

    * 2D and 3D Beam-Column Elements
    * 2D and 3D Quad Elements
    * 2D and 3D Tri Elements
    * 8 Node Brick Elements
    * 4 Node Tetrahedron Elements



Installation

::

  python -m pip install vfo

  python -m pip install --user vfo
  

To upgrade the package installation

::
 
  python -m pip install --upgrade vfo

  python -m pip install --user --upgrade vfo
   
   
The following two commands are needed to visualize the model, as shown below:

::

   # import vfo rendering module
   import vfo.vfo as vfo
   
   # render the model after defining all the nodes and elements
   vfo.plot_model()

   # plot mode shape
   vfo.plot_modeshape(modenumber=3)
   

.. image:: /_static/ModelVisualization_Intro.png

Following are commands and development guide related to model visualization:

#. :doc:`installation`
#. :doc:`createODB`
#. :doc:`saveFiberData2D`
#. :doc:`plot_model`
#. :doc:`plot_modeshape`
#. :doc:`plot_deformedshape`
#. :doc:`animate_deformedshape`
#. :doc:`plot_fiberResponse2D`
#. :doc:`animate_fiberResponse2D`
#. :doc:`plotting_OpenSeesTcl`

.. toctree::
   :maxdepth: 1
   :hidden:

   installation
   createODB
   saveFiberData2D
   plot_model
   plot_modeshape
   plot_deformedshape
   animate_deformedshape
   plot_fiberResponse2D
   animate_fiberResponse2D
   plotting_OpenSeesTcl



