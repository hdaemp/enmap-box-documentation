.. _Fit CatBoostClassifier:

**********************
Fit CatBoostClassifier
**********************

Implementation of the scikit-learn API for `CatBoost <https://catboost.ai/en/docs/>`_ `classifier <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-classifier>`_.

**Parameters**


:guilabel:`Classifier` [string]
    Scikit-learn python code. See `CatBoostClassifier <https://catboost.ai/en/docs/concepts/python-reference_catboostclassifier>`_ for information on different parameters.

    Default::

        from catboost import CatBoostClassifier
        classifier = CatBoostClassifier(n_estimators=100)

:guilabel:`Training dataset` [file]
    `Training dataset <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-training-dataset>`_ `pickle file <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-pickle-file>`_ used for fitting the `classifier <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-classifier>`_. If not specified, an unfitted classifier is created.

**Outputs**


:guilabel:`Output classifier` [fileDestination]
    Destination `pickle file <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-pickle-file>`_.

**Command-line usage**

``>qgis_process help enmapbox:FitCatboostclassifier``::

    ----------------
    Arguments
    ----------------
    
    classifier: Classifier
    	Default value:	from catboost import CatBoostClassifier
    classifier = CatBoostClassifier(n_estimators=100)
    	Argument type:	string
    	Acceptable values:
    		- String value
    dataset: Training dataset (optional)
    	Argument type:	file
    	Acceptable values:
    		- Path to a file
    outputClassifier: Output classifier
    	Argument type:	fileDestination
    	Acceptable values:
    		- Path for new file
    
    ----------------
    Outputs
    ----------------
    
    outputClassifier: <outputFile>
    	Output classifier
    
    