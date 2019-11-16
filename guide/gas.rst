.. _gas:

怎么设置 ``gas limit`` 和 ``gas price``?
===========================================

It is quite simple and easy.



Gas limit
---------

As a **BRIEF SUMMARY**:

   Gas is metering and fuel for using the Ethereum.
   ``Gas limit`` is the maximum number of gas used
   to manually set up an Ethereum transaction.

   For transactions related to **Beyou Network**, here is a form:

   ===========================================================  =========
   Usage                                                        Minimum
   ===========================================================  =========
   Stoken transfer                                            100,000
   Join the whitelist                                           600,000
   :ref:`get_1001stoken2`                                        200,000
   :ref:`stoken2_sale`                                           6,000,000
   Withdraw dividend from :ref:`stoken2_shareholders_contract`   300,000
   ===========================================================  =========

   Gas will not be wasted,
   the actual miner fee will only be calculated on demand,
   and the remaining portion will be automatically returned
   to the wallet balance.

.. NOTE::
   There is an article here `Ethereum, Gas, Fuel & Fees. (English, by Joseph Chow)`_,
   that can be used as an extended reading material.

   .. _Ethereum, Gas, Fuel & Fees. (English, by Joseph Chow):
       https://media.consensys.net/ethereum-gas-fuel-and-fees-3333e17fe1dc


Gas price
---------

``Gas price`` is the price of gas, its unit is ``gwei``.

Generally speaking, the higher the price is set,
the faster the Ethereum miners will process your transaction.
But reasonable settings can avoid unnecessary waste
without having to grab time.

There is a website `ETH Gas Station`_ you should know,
you can read the current ``Gas price`` easily.

.. _ETH Gas Station:
   https://ethgasstation.info/


.. image:: /_static/guide/gas.png
   :width: 100 %
   :alt: formula.gif
   :align: center


Both **FAST** and **STANDARD** is recommended.

