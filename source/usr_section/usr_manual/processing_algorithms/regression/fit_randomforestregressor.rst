.. _Fit RandomForestRegressor:

*************************
Fit RandomForestRegressor
*************************

A random forest `regressor <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-regressor>`_.
A random forest is a meta `estimator <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-estimator>`_ that fits a number of classifying decision trees on various sub-`samples <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-sample>`_ of the `dataset <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-dataset>`_ and uses averaging to improve the predictive accuracy and control over-fitting. The sub-`sample <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-sample>`_ size is controlled with the max_samples parameter if bootstrap=True (default), otherwise the whole dataset is used to build each tree.

**Parameters**


:guilabel:`Regressor` [string]
    Scikit-learn python code. See `RandomForestRegressor <https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestRegressor.html>`_ for information on different parameters.

    Default::

        from sklearn.ensemble import RandomForestRegressor
        regressor = RandomForestRegressor(n_estimators=100, oob_score=True)

:guilabel:`Training dataset` [file]
    `Training dataset <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-training-dataset>`_ `pickle file <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-pickle-file>`_ used for fitting the `classifier <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-classifier>`_. If not specified, an unfitted classifier is created.

**Outputs**


:guilabel:`Output regressor` [fileDestination]
    Destination `pickle file <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-pickle-file>`_.

**Command-line usage**

``>qgis_process help enmapbox:FitRandomforestregressor``::

    ----------------
    Arguments
    ----------------
    
    regressor: Regressor
    	Default value:	from sklearn.ensemble import RandomForestRegressor
    regressor = RandomForestRegressor(n_estimators=100, oob_score=True)
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
    
    