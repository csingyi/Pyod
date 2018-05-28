.. pyod documentation master file, created by
   sphinx-quickstart on Sun May 27 10:56:38 2018.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

PyOD Documentation
================================
.. image:: https://badge.fury.io/py/pyod.svg
    :target: https://badge.fury.io/py/pyod
.. image:: https://readthedocs.org/projects/pyod/badge/?version=latest
    :target: https://pyod.readthedocs.io/en/latest/?badge=latest
    :alt: Documentation Status
.. image:: https://travis-ci.org/yzhao062/Pyod.svg?branch=master
    :target: https://travis-ci.org/yzhao062/Pyod
.. image:: https://coveralls.io/repos/github/yzhao062/Pyod/badge.svg?branch=master
    :target: https://coveralls.io/github/yzhao062/Pyod?branch=master
.. image:: https://img.shields.io/github/stars/yzhao062/Pyod.svg
    :alt: GitHub stars
    :target: https://github.com/yzhao062/Pyod
.. image:: https://img.shields.io/github/forks/yzhao062/Pyod.svg
    :alt: GitHub forks
    :target: https://github.com/yzhao062/Pyod

**Py**\ thon \ **O**\ utlier \ **D**\ etection (PyOD) is a Python-based toolkit to identify outliers in data with both unsupervised and supervised algorithms.
It strives to provide unified APIs across for different anomaly detection algorithms.
The toolkit consists of three major groups of functionalities:

1. Outlier detection algorithms
    * Local Outlier Factor, LOF [1] :class:`pyod.models.lof.LOF`
    * Isolation Forest, iForest [2] :class:`pyod.models.iforest.IForest`
    * One-Class Support Vector Machines [3] :class:`pyod.models.ocsvm.OCSVM`
    * kNN Outlier Detection :class:`pyod.models.knn.KNN`
    * Average KNN Outlier Detection :class:`pyod.models.knn.KNN`
    * Median KNN Outlier Detection :class:`pyod.models.knn.KNN`
    * Broken, to fix: Global-Local Outlier Score From Hierarchies [4]
    * Histogram-based Outlier Score, HBOS [5] :class:`pyod.models.hbos.HBOS`
    * Angle-Based Outlier Setection, ABOD [7] :class:`pyod.models.abod.ABOD`

2. Outlier ensemble frameworks :mod:`pyod.models.combination`.
    * Feature bagging
    * Average of Maximum (AOM) [6] :func:`pyod.models.combination.aom`
    * Maximum of Average (MOA) [6] :func:`pyod.models.combination.moa`
    * Threshold Sum (Thresh) [6]

3. Outlier detection utility functions. See :mod:`pyod.utils`.
    * :func:`pyod.utils.utility.scores_to_lables`: converting raw outlier scores to binary labels
    * :func:`pyod.utils.utility.precision_n_scores`: one of the popular evaluation metrics for outlier mining (precision @ rank n)
    * :func:`pyod.utils.load_data.generate_data`: generate pseudo data for outlier detection experiment

More anomaly detection related resources, e.g., books, papers and videos,
can be found at `anomaly-detection-resources <https://github.com/yzhao062/anomaly-detection-resources>`_.

Contents
====================

.. toctree::
   :maxdepth: 2

   install
   example
   api

Check `Github Repository <https://github.com/yzhao062/Pyod>`_
and `PyPI <https://pypi.org/project/pyod/>`_ for more information.

PyOD has been successfully used in various academic researches [8, 9] and under active development.
However, full documentation and unit tests are temporarily unavailable yet planned for future release.
The purpose of the toolkit is for quick exploration. Using it as the final output should be cautious.
Fine-tunning may be needed to generate meaningful results.

Reference
++++++++++++

[1] Breunig, M.M., Kriegel, H.P., Ng, R.T. and Sander, J., 2000, May. LOF: identifying density-based local outliers. In *ACM SIGMOD Record*, pp. 93-104. ACM.

[2] Liu, F.T., Ting, K.M. and Zhou, Z.H., 2008, December. Isolation forest. In *ICDM '08*, pp. 413-422. IEEE.

[3] Ma, J. and Perkins, S., 2003, July. Time-series novelty detection using one-class support vector machines. In *IJCNN' 03*, pp. 1741-1745. IEEE.

[4] Campello, R.J., Moulavi, D., Zimek, A. and Sander, J., 2015. Hierarchical density estimates for data clustering, visualization, and outlier detection. *TKDD*, 10(1), pp.5.

[5] Goldstein, M. and Dengel, A., 2012. Histogram-based outlier score (hbos): A fast unsupervised anomaly detection algorithm. In *KI-2012: Poster and Demo Track*, pp.59-63.

[6] Aggarwal, C.C. and Sathe, S., 2015. Theoretical foundations and algorithms for outlier ensembles.*ACM SIGKDD Explorations Newsletter*, 17(1), pp.24-47.

[7] Kriegel, H.P. and Zimek, A., 2008, August. Angle-based outlier detection in high-dimensional data. In *KDD '08*, pp. 444-452. ACM.

[8] Y. Zhao and M.K. Hryniewicki, "XGBOD: Improving Supervised Outlier Detection with Unsupervised Representation Learning," *IEEE International Joint Conference on Neural Networks*, 2018.

[9] Y. Zhao and M.K. Hryniewicki, "DCSO: Dynamic Combination of Detector Scores for Outlier Ensembles," *ACM SIGKDD Workshop on Outlier Detection De-constructed*, 2018. Submitted, under review.

==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`