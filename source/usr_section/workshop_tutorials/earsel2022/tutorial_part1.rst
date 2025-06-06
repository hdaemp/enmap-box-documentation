.. include:: /icon_links.rst

.. _tutorial_earsel_part1:

12th EARSeL Imaging Spectroscopy Workshop - Part I: Introduction into the EnMAP-Box
###################################################################################

**Authors:**  Andreas Rabe

**Date:** 17/06/2022

**EnMAP-Box 3:** version 3.10

**QGIS:** version 3.24

Introduction
************

Abstract
    In this tutorial we will show the basic components of the EnMAP-Box.
    Participants will learn how to manage, visualize and process raster and vector data inside the EnMAP-Box.
    We will detail the multiple-viewer concept of the EnMAP-Box, that allows the exploration of data in different
    visualizations at the same time.
    Here we will especially highlight, how we capitalize on the spectral characteristics of optical (hyperspectral)
    EO data, e.g. by correctly plotting pixel profiles against the given center wavelength,
    or by quickly selecting target bands for visualization. Finally, we will perform a Classification Analysis Workflow
    using PRISMA or (simulated) EnMAP data to illustrate EO data processing.

Requirements
    This tutorial requires version 3.10+ of the EnMAP-Box 3 running in QGIS 3.24+.

Data
    :download:`You can download the data for this exercise here:`
    https://box.hu-berlin.de/f/2ecf8943d6fa4474bf38/?dl=1

    The tutorial dataset contains a PRISMA L2D image over Berlin, Germany,
    as well as a point based landcover reference sample.

    .. csv-table::
       :header-rows: 1
       :delim: ;
       :widths: auto

       Type; Filename; Description
       Raster; :file:`PRS_L2D_STD_20201107101404_20201107101408_0001_SPECTRAL.tif`; Surface reflectance, coregistersed, hyperspectral cube from the PRISMA sensor with a spatial resolution of 30m, 234 bands, and 1281x1238 pixels
       Vector; :file:`landcover_berlin_point.gpkg`; 58 landcover reference points

    .. figure:: img/dataset.png
       :width: 99%
       :align: center

    For more details on PRISMA data see: https://prisma.asi.it/

Exercise A: Visualize PRISMA data inside the EnMAP-Box
******************************************************

Open the PRISMA raster
    In the EnMAP-Box, open the `PRS_L2D_STD_20201107101404_20201107101408_0001_SPECTRAL.tif` raster and visualize it
    in a map view using drag&drop.

    .. # earsel2022_part1_exerciseA_01.mp4

    .. raw:: html

       <figure class="video_container">
          <video width="100%" controls="true" allowfullscreen="true">
              <source src="https://box.hu-berlin.de/f/b90072db612f462e81e6/?dl=1" type="video/mp4">
          </video>
       </figure>

Style the PRISMA layer using an RGB visualization
    We can improve the visualization using the :guilabel:`Raster Layer Styling` panel.

    As the PRISMA layer contains information about the center wavelength location for each band,
    we can directly choose from a list of predefined RGB band combinations,
    e.g. :guilabel:`Natural color (R-G-B)` for showing Red band, Green band and Blue band as an RGB visualization,
    or :guilabel:`Agricultural 1 (S1-N-B)` for showing SWIR 1 band, NIR band Blue band as an RGB visualization.

    Use the :guilabel:`A`, :guilabel:`B`, ..., :guilabel:`S2` buttons, to select individual PRISMA bands that best match the predefined
    broad bands from the Sentinel-2 sensor, e.g. :guilabel:`N` is associated with the Sentinel-2 NIR band at 833 nanometers.

    Use the widgets in the :guilabel:`Min / Max Value Settings` to interactively alter and improve the contrast
    stretch.

    .. # earsel2022_part1_exerciseA_02.mp4

    .. raw:: html

       <figure class="video_container">
          <video width="100%" controls="true" allowfullscreen="true">
              <source src="https://box.hu-berlin.de/f/4e27f197bd5440f0944a/?dl=1" type="video/mp4">
          </video>
       </figure>

Use a singleband gray visualization to identify bad bands
    Due to atmospheric conditions, the PRISMA raster may contain bad bands,
    which can be identified easily using a singleband gray visualization.

    In the :guilabel:`Raster Layer Styling` panel select the :guilabel:`Gray` tab to change the visualization.

    Use the band selection slider or the band selection combobox (together with the Arrow-Up and Arrow-Down keys)
    to browse the PRISMA bands and identify potential bad bands.

    As before, you can also use the :guilabel:`A`, :guilabel:`B`, ..., :guilabel:`S2` buttons.

    .. # earsel2022_part1_exerciseA_03.mp4

    .. raw:: html

       <figure class="video_container">
          <video width="100%" controls="true" allowfullscreen="true">
              <source src="https://box.hu-berlin.de/f/88a2a9a7b21342ae9167/?dl=1" type="video/mp4">
          </video>
       </figure>

Plot spectral profiles and show cursor location values
    Use the :guilabel:`Identify` map tool to plot PRISMA spectral profiles and query band values for the selected
    location.

    In the :guilabel:`Spectral Profile Sources` panel you can easily alter the plot style.

    .. # earsel2022_part1_exerciseA_04.mp4

    .. raw:: html

       <figure class="video_container">
          <video width="100%" controls="true" allowfullscreen="true">
              <source src="https://box.hu-berlin.de/f/2e5181e5cc8d4c109d8a/?dl=1" type="video/mp4">
          </video>
       </figure>

Exercise B: Perform a land cover classification
***********************************************

Derive a landcover map for the PRISMA raster
    Use the :guilabel:`Classification workflow` algorithm to perform a full landcover classification.
    This includes training data preparation, fitting a Random Forest Classifier, and predicting landcover classes
    and class probabilities.

    The original PRISMA raster and the derived classification and class probabilities can be visualized next to each
    other using multiple map views.

    Finally, visualize the probabilities for the classes `impervious`, `tree` and `water` as RGB multiband color.

    .. # earsel2022_part1_exerciseB_01.mp4

    .. raw:: html

       <figure class="video_container">
          <video width="100%" controls="true" allowfullscreen="true">
              <source src="https://box.hu-berlin.de/f/a2d9d08ea4964d9cbb84/?dl=1" type="video/mp4">
          </video>
       </figure>

Visualize the predicted maps
    Use the :guilabel:`Classification Statistics` app to visualize the derived classification map.

    .. # earsel2022_part1_exerciseB_02.mp4

    .. raw:: html

       <figure class="video_container">
          <video width="100%" controls="true" allowfullscreen="true">
              <source src="https://box.hu-berlin.de/f/8f41d7999051406cab4f/?dl=1" type="video/mp4">
          </video>
       </figure>

    Use the :guilabel:`Class Fraction/Probability Statistics` app to visualize the derived class probability map.

    .. # earsel2022_part1_exerciseB_03.mp4

    .. raw:: html

       <figure class="video_container">
          <video width="100%" controls="true" allowfullscreen="true">
              <source src="https://box.hu-berlin.de/f/ecbe7a742ecb4ff4b0f6/?dl=1" type="video/mp4">
          </video>
       </figure>

View the fitted Random Forest Classifier model
    The training data and the fitted model can be explored inside the :guilabel:`Data Sources` panel.

    .. # earsel2022_part1_exerciseB_04.mp4

    .. raw:: html

       <figure class="video_container">
          <video width="100%" controls="true" allowfullscreen="true">
              <source src="https://box.hu-berlin.de/f/05cb85dff61c453ca587/?dl=1" type="video/mp4">
          </video>
       </figure>