.. _Fit LGBMRegressor:

*****************
Fit LGBMRegressor
*****************

Implementation of the scikit-learn API for `LightGBM  <https://lightgbm.readthedocs.io/>`_ `regressor <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-regressor>`_.

**Parameters**


:guilabel:`Regressor` [string]
    Scikit-learn python code. See `LGBMRegressor <https://lightgbm.readthedocs.io/en/latest/pythonapi/lightgbm.LGBMRegressor.html#lightgbm-lgbmregressor>`_ for information on different parameters.

    Default::

        from lightgbm import LGBMRegressor
        
        regressor = LGBMRegressor(n_estimators=100)

:guilabel:`Training dataset` [file]
    `Training dataset <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-training-dataset>`_ `pickle file <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-pickle-file>`_ used for fitting the `classifier <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-classifier>`_. If not specified, an unfitted classifier is created.

**Outputs**


:guilabel:`Output regressor` [fileDestination]
    Destination `pickle file <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-pickle-file>`_.

**Command-line usage**

``>qgis_process help enmapbox:FitLgbmregressor``::

    ----------------
    Arguments
    ----------------
    
    regressor: Regressor
    	Default value:	from lightgbm import LGBMRegressor
    
    regressor = LGBMRegressor(n_estimators=100)
    	Argument type:	string
    	Acceptable values:
    		- String value
    dataset: Training dataset (optional)
    	Argument type:	file
    	Acceptable values:
    		- Path to a file
    outputRegressor: Output regressor
    	Argument type:	fileDestination
    	Acceptable values:
    		- Path for new file
    
    ----------------
    Outputs
    ----------------
    
    outputRegressor: <outputFile>
    	Output regressor
    
    