.. _Create regression dataset (from continuous-valued vector layer and feature raster):

**********************************************************************************
Create regression dataset (from continuous-valued vector layer and feature raster)
**********************************************************************************

Create a `regression <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-regression>`_ `dataset <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-dataset>`_ by sampling data and store the result as a `pickle file <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-pickle-file>`_.

**Parameters**


:guilabel:`Continuous-valued vector layer` [vector]
    `Continuous-valued vector layer <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-continuous-valued-vector-layer>`_ specifying `sample <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-sample>`_ locations and `target <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-target>`_ data `y <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-y>`_. If required, the `layer <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-layer>`_ is reprojected and rasterized internally to match the `feature <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-feature>`_ raster `grid <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-grid>`_.


:guilabel:`Raster layer with features` [raster]
    `Raster layer <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-raster-layer>`_ used for sampling `feature <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-feature>`_ data `X <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-x>`_.


:guilabel:`Fields with targets` [field]
    Fields used as `target <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-target>`_ data `y <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-y>`_. If not selected, the `fields <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-field>`_ defined by the renderer are used. If those are also not specified, an error is raised.

**Outputs**


:guilabel:`Output dataset` [fileDestination]
    Destination `pickle file <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-pickle-file>`_.

**Command-line usage**

``>qgis_process help enmapbox:CreateRegressionDatasetFromContinuousvaluedVectorLayerAndFeatureRaster``::

    ----------------
    Arguments
    ----------------
    
    continuousVector: Continuous-valued vector layer
    	Argument type:	vector
    	Acceptable values:
    		- Path to a vector layer
    featureRaster: Raster layer with features
    	Argument type:	raster
    	Acceptable values:
    		- Path to a raster layer
    targetFields: Fields with targets (optional)
    	Argument type:	field
    	Acceptable values:
    		- The name of an existing field
    		- ; delimited list of existing field names
    outputRegressionDataset: Output dataset
    	Argument type:	fileDestination
    	Acceptable values:
    		- Path for new file
    
    ----------------
    Outputs
    ----------------
    
    outputRegressionDataset: <outputFile>
    	Output dataset
    
    