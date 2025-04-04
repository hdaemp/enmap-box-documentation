.. _Create spectral indices:

***********************
Create spectral indices
***********************

Create a stack of `Awesome Spectral Indices <https://awesome-ee-spectral-indices.readthedocs.io/en/latest/list.html>`_ and/or custom indices.
Credits: the Awesome Spectral Indices project provides a ready-to-use curated list of Spectral Indices for Remote Sensing applications, maintained by `David Montero Loaiza <https://github.com/davemlz>`_.

**Parameters**


:guilabel:`Raster layer` [raster]
    A `spectral raster layer <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-spectral-raster-layer>`_.


:guilabel:`Indices` [string]
    The list of indices to be created. Usage examples:
    Create (predefined) NDVI: <code>NDVI</code>
    Create stack of NDVI and EVI: <code>NDVI, EVI</code>
    Create custom index: <code>MyNDVI = (N - R) / (N + R)</code>
    See the full list of predefined  `Awesome Spectral Indices <https://awesome-ee-spectral-indices.readthedocs.io/en/latest/list.html>`_.

    Default: *NDVI*


:guilabel:`Scale factor` [number]
    Spectral reflectance scale factor. Some indices require data to be scaled into the 0 to 1 range. If your data is scaled differently, specify an appropriate scale factor.E.g. for Int16 data scaled into the 0 to 10000 range, use a value of 10000.
    

**Outputs**


:guilabel:`Output VRT layer` [rasterDestination]
    VRT file destination.

**Command-line usage**

``>qgis_process help enmapbox:CreateSpectralIndices``::

    ----------------
    Arguments
    ----------------
    
    raster: Raster layer
    	Argument type:	raster
    	Acceptable values:
    		- Path to a raster layer
    indices: Indices
    	Default value:	NDVI
    	Argument type:	string
    	Acceptable values:
    		- String value
    scale: Scale factor (optional)
    	Argument type:	number
    	Acceptable values:
    		- A numeric value
    A: Aerosols band (optional)
    	Default value:	-1
    	Argument type:	band
    	Acceptable values:
    		- Integer value representing an existing raster band number
    B: Blue band (optional)
    	Default value:	-1
    	Argument type:	band
    	Acceptable values:
    		- Integer value representing an existing raster band number
    G: Green band (optional)
    	Default value:	-1
    	Argument type:	band
    	Acceptable values:
    		- Integer value representing an existing raster band number
    R: Red band (optional)
    	Default value:	-1
    	Argument type:	band
    	Acceptable values:
    		- Integer value representing an existing raster band number
    RE1: Red Edge 1 band (optional)
    	Default value:	-1
    	Argument type:	band
    	Acceptable values:
    		- Integer value representing an existing raster band number
    RE2: Red Edge 2 band (optional)
    	Default value:	-1
    	Argument type:	band
    	Acceptable values:
    		- Integer value representing an existing raster band number
    RE3: Red Edge 3 band (optional)
    	Default value:	-1
    	Argument type:	band
    	Acceptable values:
    		- Integer value representing an existing raster band number
    RE4: Red Edge 4 band (optional)
    	Default value:	-1
    	Argument type:	band
    	Acceptable values:
    		- Integer value representing an existing raster band number
    N: NIR band (optional)
    	Default value:	-1
    	Argument type:	band
    	Acceptable values:
    		- Integer value representing an existing raster band number
    S1: SWIR 1 band (optional)
    	Default value:	-1
    	Argument type:	band
    	Acceptable values:
    		- Integer value representing an existing raster band number
    S2: SWIR 2 band (optional)
    	Default value:	-1
    	Argument type:	band
    	Acceptable values:
    		- Integer value representing an existing raster band number
    T1: Thermal 1 band (optional)
    	Default value:	-1
    	Argument type:	band
    	Acceptable values:
    		- Integer value representing an existing raster band number
    T2: Thermal 2 band (optional)
    	Default value:	-1
    	Argument type:	band
    	Acceptable values:
    		- Integer value representing an existing raster band number
    L: Canopy background adjustment (optional)
    	Default value:	1
    	Argument type:	number
    	Acceptable values:
    		- A numeric value
    g: Gain factor (optional)
    	Default value:	2.5
    	Argument type:	number
    	Acceptable values:
    		- A numeric value
    C1: Coefficient 1 for the aerosol resistance term (optional)
    	Default value:	6
    	Argument type:	number
    	Acceptable values:
    		- A numeric value
    C2: Coefficient 2 for the aerosol resistance term (optional)
    	Default value:	7.5
    	Argument type:	number
    	Acceptable values:
    		- A numeric value
    cexp: Exponent used for OCVI (optional)
    	Default value:	1.16
    	Argument type:	number
    	Acceptable values:
    		- A numeric value
    nexp: Exponent used for GDVI (optional)
    	Default value:	2
    	Argument type:	number
    	Acceptable values:
    		- A numeric value
    alpha: Weighting coefficient used for WDRVI (optional)
    	Default value:	0.1
    	Argument type:	number
    	Acceptable values:
    		- A numeric value
    gamma: Weighting coefficient used for ARVI (optional)
    	Default value:	1
    	Argument type:	number
    	Acceptable values:
    		- A numeric value
    sla: Soil line slope (optional)
    	Default value:	1
    	Argument type:	number
    	Acceptable values:
    		- A numeric value
    slb: Soil line intercept (optional)
    	Default value:	0
    	Argument type:	number
    	Acceptable values:
    		- A numeric value
    outputVrt: Output VRT layer
    	Argument type:	rasterDestination
    	Acceptable values:
    		- Path for new raster layer
    
    ----------------
    Outputs
    ----------------
    
    outputVrt: <outputRaster>
    	Output VRT layer
    
    