.. _Spectral resampling (to EnMAP):

******************************
Spectral resampling (to EnMAP)
******************************

Spectrally resample a `spectral raster layer <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-spectral-raster-layer>`_ by applying `spectral response function <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-spectral-response-function>`_ convolution.
For more information see the `EnMAP <https://www.enmap.org/>`_ mission website.

**Parameters**


:guilabel:`Spectral raster layer` [raster]
    A `spectral raster layer <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-spectral-raster-layer>`_ to be resampled.


:guilabel:`Spectral response function` [string]
    Python code specifying the `spectral response function <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-spectral-response-function>`_.

    Default::

        from collections import OrderedDict
        
        responses = OrderedDict()
        wavelength = [460, 465, 470, 475, 479, 484, 489, 494, 499, 503, 508, 513, 518, 523, 528, 533, 538, 543, 549, 554, 559, 565, 570, 575, 581, 587, 592, 598, 604, 610, 616, 622, 628, 634, 640, 646, 653, 659, 665, 672, 679, 685, 692, 699, 706, 713, 720, 727, 734, 741, 749, 756, 763, 771, 778, 786, 793, 801, 809, 817, 824, 832, 840, 848, 856, 864, 872, 880, 888, 896, 915, 924, 934, 944, 955, 965, 975, 986, 997, 1007, 1018, 1029, 1040, 1051, 1063, 1074, 1086, 1097, 1109, 1120, 1132, 1144, 1155, 1167, 1179, 1191, 1203, 1215, 1227, 1239, 1251, 1263, 1275, 1287, 1299, 1311, 1323, 1522, 1534, 1545, 1557, 1568, 1579, 1590, 1601, 1612, 1624, 1634, 1645, 1656, 1667, 1678, 1689, 1699, 1710, 1721, 1731, 1742, 1752, 1763, 1773, 1783, 2044, 2053, 2062, 2071, 2080, 2089, 2098, 2107, 2115, 2124, 2133, 2141, 2150, 2159, 2167, 2176, 2184, 2193, 2201, 2210, 2218, 2226, 2234, 2243, 2251, 2259, 2267, 2275, 2283, 2292, 2300, 2308, 2315, 2323, 2331, 2339, 2347, 2355, 2363, 2370, 2378, 2386, 2393, 2401, 2409]
        fwhm = [5.8, 5.8, 5.8, 5.8, 5.8, 5.8, 5.8, 5.8, 5.8, 5.8, 5.9, 5.9, 6.0, 6.0, 6.1, 6.1, 6.2, 6.2, 6.3, 6.4, 6.4, 6.5, 6.6, 6.6, 6.7, 6.8, 6.9, 6.9, 7.0, 7.1, 7.2, 7.3, 7.3, 7.4, 7.5, 7.6, 7.7, 7.8, 7.9, 7.9, 8.0, 8.1, 8.2, 8.3, 8.4, 8.4, 8.5, 8.6, 8.7, 8.7, 8.8, 8.9, 8.9, 9.0, 9.1, 9.1, 9.2, 9.3, 9.3, 9.4, 9.4, 9.5, 9.5, 9.6, 9.6, 9.6, 9.6, 9.7, 9.7, 9.7, 11.8, 11.9, 12.1, 12.2, 12.4, 12.5, 12.7, 12.8, 12.9, 13.1, 13.2, 13.3, 13.4, 13.5, 13.6, 13.7, 13.8, 13.9, 14.0, 14.0, 14.1, 14.1, 14.2, 14.2, 14.3, 14.3, 14.3, 14.4, 14.4, 14.4, 14.4, 14.4, 14.4, 14.4, 14.4, 14.4, 14.4, 13.7, 13.6, 13.6, 13.5, 13.5, 13.4, 13.4, 13.3, 13.2, 13.2, 13.1, 13.1, 13.0, 12.9, 12.9, 12.8, 12.8, 12.7, 12.7, 12.6, 12.5, 12.5, 12.4, 12.4, 12.3, 10.9, 10.8, 10.8, 10.7, 10.7, 10.6, 10.6, 10.5, 10.5, 10.4, 10.4, 10.4, 10.3, 10.3, 10.2, 10.2, 10.1, 10.1, 10.1, 10.0, 10.0, 9.9, 9.9, 9.9, 9.8, 9.8, 9.7, 9.7, 9.7, 9.6, 9.6, 9.6, 9.5, 9.5, 9.4, 9.4, 9.4, 9.3, 9.3, 9.3, 9.2, 9.2, 9.1, 9.1, 9.1]
        for w, f in zip(wavelength, fwhm):
            responses[w] = f

:guilabel:`Save spectral response function` [boolean]
    Whether to save the `spectral response function library <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-spectral-response-function-library>`_ as *.srf.gpkg sidecar file.

    Default: *False*

**Outputs**


:guilabel:`Output raster layer` [rasterDestination]
    Raster file destination.

**Command-line usage**

``>qgis_process help enmapbox:SpectralResamplingToEnmap``::

    ----------------
    Arguments
    ----------------
    
    raster: Spectral raster layer
    	Argument type:	raster
    	Acceptable values:
    		- Path to a raster layer
    response: Spectral response function
    	Default value:	from collections import OrderedDict
    
    responses = OrderedDict()
    wavelength = [460, 465, 470, 475, 479, 484, 489, 494, 499, 503, 508, 513, 518, 523, 528, 533, 538, 543, 549, 554, 559, 565, 570, 575, 581, 587, 592, 598, 604, 610, 616, 622, 628, 634, 640, 646, 653, 659, 665, 672, 679, 685, 692, 699, 706, 713, 720, 727, 734, 741, 749, 756, 763, 771, 778, 786, 793, 801, 809, 817, 824, 832, 840, 848, 856, 864, 872, 880, 888, 896, 915, 924, 934, 944, 955, 965, 975, 986, 997, 1007, 1018, 1029, 1040, 1051, 1063, 1074, 1086, 1097, 1109, 1120, 1132, 1144, 1155, 1167, 1179, 1191, 1203, 1215, 1227, 1239, 1251, 1263, 1275, 1287, 1299, 1311, 1323, 1522, 1534, 1545, 1557, 1568, 1579, 1590, 1601, 1612, 1624, 1634, 1645, 1656, 1667, 1678, 1689, 1699, 1710, 1721, 1731, 1742, 1752, 1763, 1773, 1783, 2044, 2053, 2062, 2071, 2080, 2089, 2098, 2107, 2115, 2124, 2133, 2141, 2150, 2159, 2167, 2176, 2184, 2193, 2201, 2210, 2218, 2226, 2234, 2243, 2251, 2259, 2267, 2275, 2283, 2292, 2300, 2308, 2315, 2323, 2331, 2339, 2347, 2355, 2363, 2370, 2378, 2386, 2393, 2401, 2409]
    fwhm = [5.8, 5.8, 5.8, 5.8, 5.8, 5.8, 5.8, 5.8, 5.8, 5.8, 5.9, 5.9, 6.0, 6.0, 6.1, 6.1, 6.2, 6.2, 6.3, 6.4, 6.4, 6.5, 6.6, 6.6, 6.7, 6.8, 6.9, 6.9, 7.0, 7.1, 7.2, 7.3, 7.3, 7.4, 7.5, 7.6, 7.7, 7.8, 7.9, 7.9, 8.0, 8.1, 8.2, 8.3, 8.4, 8.4, 8.5, 8.6, 8.7, 8.7, 8.8, 8.9, 8.9, 9.0, 9.1, 9.1, 9.2, 9.3, 9.3, 9.4, 9.4, 9.5, 9.5, 9.6, 9.6, 9.6, 9.6, 9.7, 9.7, 9.7, 11.8, 11.9, 12.1, 12.2, 12.4, 12.5, 12.7, 12.8, 12.9, 13.1, 13.2, 13.3, 13.4, 13.5, 13.6, 13.7, 13.8, 13.9, 14.0, 14.0, 14.1, 14.1, 14.2, 14.2, 14.3, 14.3, 14.3, 14.4, 14.4, 14.4, 14.4, 14.4, 14.4, 14.4, 14.4, 14.4, 14.4, 13.7, 13.6, 13.6, 13.5, 13.5, 13.4, 13.4, 13.3, 13.2, 13.2, 13.1, 13.1, 13.0, 12.9, 12.9, 12.8, 12.8, 12.7, 12.7, 12.6, 12.5, 12.5, 12.4, 12.4, 12.3, 10.9, 10.8, 10.8, 10.7, 10.7, 10.6, 10.6, 10.5, 10.5, 10.4, 10.4, 10.4, 10.3, 10.3, 10.2, 10.2, 10.1, 10.1, 10.1, 10.0, 10.0, 9.9, 9.9, 9.9, 9.8, 9.8, 9.7, 9.7, 9.7, 9.6, 9.6, 9.6, 9.5, 9.5, 9.4, 9.4, 9.4, 9.3, 9.3, 9.3, 9.2, 9.2, 9.1, 9.1, 9.1]
    for w, f in zip(wavelength, fwhm):
        responses[w] = f
    	Argument type:	string
    	Acceptable values:
    		- String value
    saveResponseFunction: Save spectral response function (optional)
    	Default value:	false
    	Argument type:	boolean
    	Acceptable values:
    		- 1 for true/yes
    		- 0 for false/no
    outputResampledRaster: Output raster layer
    	Argument type:	rasterDestination
    	Acceptable values:
    		- Path for new raster layer
    
    ----------------
    Outputs
    ----------------
    
    outputResampledRaster: <outputRaster>
    	Output raster layer
    
    