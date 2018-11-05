.. _sec:dbns:

Dynamic Bayesian Networks: Code Examples
========================================

-  

   .. raw:: latex

      \hyperref[sec:dbns:datastreams]{Data Streams}

-  

   .. raw:: latex

      \hyperref[sec:dbns:variables]{Dynamic Random Variables}

-  

   .. raw:: latex

      \hyperref[sec:dbns:dbns]{Dynamic Bayesian networks}

   -  

      .. raw:: latex

         \hyperref[sec:dbns:dbns:creating]{Creating Dynamic Bayesian networks}

   -  

      .. raw:: latex

         \hyperref[sec:dbns:dbns:creatingLatent]{Creating Dynamic Bayesian Networks with Latent Variables}

   -  

      .. raw:: latex

         \hyperref[sec:dbns:dbns:modif]{Modifying Dynamic Bayesian Networks}

-  

   .. raw:: latex

      \hyperref[sec:dbns:sampling]{Sampling from Dynamic Bayesian Networks}

-  

   .. raw:: latex

      \hyperref[sec:dbns:inference]{Inference Algorithms for Dynamic Bayesian Networks}

   -  

      .. raw:: latex

         \hyperref[sec:dbns:inference:dmap]{The Dynamic MAP Inference}

   -  

      .. raw:: latex

         \hyperref[sec:dbns:inference:dvmp]{The Dynamic Variational Message Passing}

   -  

      .. raw:: latex

         \hyperref[sec:dbns:inference:dis]{The Dynamic Importance Sampling}

-  

   .. raw:: latex

      \hyperref[sec:dbns:learning]{Dynamic Learning Algorithms}

   -  

      .. raw:: latex

         \hyperref[sec:dbns:learning:ml]{Maximum Likelihood for DBNs}

   -  

      .. raw:: latex

         \hyperref[sec:dbns:learning:sv]{Streaming Variational Bayes for DBNs}

.. _sec:dbns:datastreams:

Data Streams
------------

In this example we show how to use the main features of a *DataStream*
object. More precisely, we show how to load a dynamic data stream and
how to iterate over the *DynamicDataInstance* objects.

.. code:: java

.. _sec:dbns:variables:

Dynamic Random Variables
------------------------

This example show the basic functionalities related to dynamic
variables.

.. code:: java

.. _sec:dbns:dbns:

Dynamic Bayesian networks
-------------------------

.. _sec:dbns:dbns:creating:

Creating Dynamic Bayesian networks
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This example creates a dynamic BN, from a dynamic data stream, with
randomly generated probability distributions, then saves it to a file.

.. code:: java

.. _sec:dbns:dbns:creatingLatent:

Creating Dynamic Bayesian Networks with Latent Variables
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This example shows how to create a BN model with hidden variables. We
simply create a BN for clustering, i.e., a naive Bayes like structure
with a single hidden variable acting as parant of all the remaining
observable variables.

.. code:: java

.. _sec:dbns:dbns:modif:

Modifying Dynamic Bayesian Networks
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This example shows how to create a BN model with hidden variables. We
This example shows how to access and modify the conditional
probabilities of a Dynamic Bayesian network model.

.. code:: java

.. _sec:dbns:sampling:

Sampling from Dynamic Bayesian Networks
---------------------------------------

This example shows how to use the *DynamicBayesianNetworkSampler* class
to randomly generate a dynamic data stream from a given Dynamic Bayesian
network.

.. code:: java

.. _sec:dbns:inference:

Inference Algorithms for Dynamic Bayesian Networks
--------------------------------------------------

.. _sec:dbns:inference:dmap:

The Dynamic MAP Inference
~~~~~~~~~~~~~~~~~~~~~~~~~

This example shows how to use the Dynamic MAP Inference algorithm.

.. code:: java

.. _sec:dbns:inference:dvmp:

The Dynamic Variational Message Passing
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This example shows how to use the Factored Frontier algorithm with
Variational Message Passing for running inference on dynamic Bayesian
networks.

.. code:: java

.. _sec:dbns:inference:dis:

The Dynamic Importance Sampling
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This example shows how to use the Factored Frontier algorithm with
Importance Sampling for running inference in dynamic Bayesian networks.

.. code:: java

.. _sec:dbns:learning:

Dynamic Learning Algorithms
---------------------------

.. _sec:dbns:learning:ml:

Maximum Likelihood for DBNs
~~~~~~~~~~~~~~~~~~~~~~~~~~~

This example shows how to learn the parameters of a dynamic Bayesian
network using maximum likelihood from a randomly sampled data stream.

.. code:: java

.. _sec:dbns:learning:sv:

Streaming Variational Bayes for DBNs
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

This example shows how to learn the parameters of a dynamic Bayesian
network using streaming variational Bayes from a randomly sampled data
stream.

.. code:: java


