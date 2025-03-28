.. _Edit raster source band properties:

**********************************
Edit raster source band properties
**********************************

Set `band <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-band>`_ properties for the given GDAL raster source. Be sure to close the raster in QGIS beforehand.

**Parameters**


:guilabel:`GDAL raster source` [file]
    GDAL raster source.


:guilabel:`Band names` [string]
    List of `band name <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-band-name>`_ strings (e.g".


:guilabel:`Center wavelength values` [string]
    List of `band <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-band>`_ `center wavelength <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-center-wavelength>`_ values in nanometers. Use nan value to unset property.


:guilabel:`Full width at half maximum (FWHM) values` [string]
    List of `band <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-band>`_ FWHM values in nanometers. Use nan value to unset property.


:guilabel:`Bad band multipliers` [string]
    List of `bad band multiplier <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-bad-band-multiplier>`_ values (BBL).


:guilabel:`Start times` [string]
    List of `band <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-band>`_ start time timestamps strings. Format is: 2009-08-20T09:44:50. Use empty string to unset property


:guilabel:`End times` [string]
    List of `band <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-band>`_ end time timestamps strings. Format is: 2009-08-20T09:44:50. Use empty string to unset property


:guilabel:`Offsets` [string]
    List of `band <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-band>`_ data offset values.


:guilabel:`Scales` [string]
    List of `band <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-band>`_ data scale/gain values.


:guilabel:`No data values` [string]
    List of `band <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-band>`_ `no data values <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-no-data-value>`_. Use None to unset property.

**Command-line usage**

``>qgis_process help enmapbox:EditRasterSourceBandProperties``::

    ----------------
    Arguments
    ----------------
    
    source: GDAL raster source
    	Argument type:	file
    	Acceptable values:
    		- Path to a file
    names: Band names (optional)
    	Argument type:	string
    	Acceptable values:
    		- String value
    wavelengths: Center wavelength values (optional)
    	Argument type:	string
    	Acceptable values:
    		- String value
    fwhms: Full width at half maximum (FWHM) values (optional)
    	Argument type:	string
    	Acceptable values:
    		- String value
    badBandMultipliers: Bad band multipliers (optional)
    	Argument type:	string
    	Acceptable values:
    		- String value
    startTimes: Start times (optional)
    	Argument type:	string
    	Acceptable values:
    		- String value
    endTimes: End times (optional)
    	Argument type:	string
    	Acceptable values:
    		- String value
    offsets: Offsets (optional)
    	Argument type:	string
    	Acceptable values:
    		- String value
    scales: Scales (optional)
    	Argument type:	string
    	Acceptable values:
    		- String value
    noDataValues: No data values (optional)
    	Argument type:	string
    	Acceptable values:
    		- String value
    
    ----------------
    Outputs
    ----------------
    
    
    