.. _Fit MeanShift:

*************
Fit MeanShift
*************

Mean shift `clustering <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-clustering>`_ using a flat kernel.
Mean shift clustering aims to discover “blobs” in a smooth density of `samples <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-sample>`_. It is a centroid-based algorithm, which works by updating candidates for centroids to be the mean of the points within a given region. These candidates are then filtered in a post-processing stage to eliminate near-duplicates to form the final set of centroids.
Seeding is performed using a binning technique for scalability.

**Parameters**


:guilabel:`Clusterer` [string]
    Scikit-learn python code. See `MeanShift <https://scikit-learn.org/stable/modules/generated/sklearn.cluster.MeanShift.html>`_ for information on different parameters.

    Default::

        from sklearn.pipeline import make_pipeline
        from sklearn.preprocessing import StandardScaler
        from sklearn.cluster import MeanShift
        
        meanShift = MeanShift()
        clusterer = make_pipeline(StandardScaler(), meanShift)
        

:guilabel:`Training dataset` [file]
    `Training dataset <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-training-dataset>`_ `pickle file <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-pickle-file>`_ used for fitting the `clusterer <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-clusterer>`_. If not specified, an unfitted clusterer is created.

**Outputs**


:guilabel:`Output clusterer` [fileDestination]
    Destination `pickle file <https://enmap-box.readthedocs.io/en/latest/general/glossary.html#term-pickle-file>`_.

**Command-line usage**

``>qgis_process help enmapbox:FitMeanshift``::

    ----------------
    Arguments
    ----------------
    
    clusterer: Clusterer
    	Default value:	from sklearn.pipeline import make_pipeline
    from sklearn.preprocessing import StandardScaler
    from sklearn.cluster import MeanShift
    
    meanShift = MeanShift()
    clusterer = make_pipeline(StandardScaler(), meanShift)
    
    	Argument type:	string
    	Acceptable values:
    		- String value
    dataset: Training dataset
    	Argument type:	file
    	Acceptable values:
    		- Path to a file
    outputClusterer: Output clusterer
    	Argument type:	fileDestination
    	Acceptable values:
    		- Path for new file
    
    ----------------
    Outputs
    ----------------
    
    outputClusterer: <outputFile>
    	Output clusterer
    
    