.. _query_stoken:

怎么查询Stoken数据
==========================

|logo_etherscan_verified| |logo_github| |logo_verified|

- 合约地址是**0x460cbb9409a024a55f2b7b7f69afd0da385ce850**
- 发布在`Tx Hash 0xd88541481a39c1...`_
- 区块号`#8623851`_
- 开源在协议`GNU General Public License v3.0`_下
- `在github仓库中查看合约代码`_
- `在Etherscan.io上查看合约`_

.. _Tx Hash 0xd88541481a39c1...:
   https://etherscan.io/tx/0x92f717e0385ec5505aac0e3a093c1f03e2bdffbb4a48d620a62cc80735ff1c83
.. _#8623851:
   https://etherscan.io/block/8623851
.. _GNU General Public License v3.0:
   https://github.com/stoken100g/contracts/blob/master/LICENSE
.. _在github仓库中查看合约代码:
   https://github.com/stoken100g/contracts/blob/master/Stoken2Panel.sol
.. _在Etherscan.io上查看合约:
   https://etherscan.io/address/0x460cbb9409a024a55f2b7b7f69afd0da385ce850#readContract

.. |logo_github| image:: /_static/logos/github.svg
   :width: 36px
   :height: 36px

.. |logo_etherscan_verified| image:: /_static/logos/etherscan_verified.svg
   :width: 36px
   :height: 36px

.. |logo_verified| image:: /_static/logos/verified.svg
   :width: 36px
   :height: 36px


**合约地址**:
``https://etherscan.io/address/0x460cbb9409a024a55f2b7b7f69afd0da385ce850#readContract``

点击 `这里`_, **查看合约**

.. _这里: https://etherscan.io/address/0x460cbb9409a024a55f2b7b7f69afd0da385ce850#readContract


Stoken统计数据
----------------

方法 #2: **stoken2**

.. image:: /_static/contract/stoken2_summary.png
   :width: 80 %
   :align: center
   :alt: stoken2_summary.png

.. NOTE::

   totalSupply
      Stoken的总量，保留六位小数

      ``1000000000`` 代表一共有 **1,000,000,000.000 Stoken**。


   whitelistCounter
      whitelisted addresses的数量, 无小数

      ``6918`` 代表一共有 6,918 个地址已经录入白名单。


   whitelistingMode
      白名单注册是否打开

      ``True`` 代表 **打开**, and ``False`` for **关闭**.

      当返回``True``时，你可以参照 :ref:`how_to_join_the_whitelist` 去参加.


   safeMode
      **安全模式** 是否打开

      ``True`` 代表 **打开**, and ``False`` for **关闭**

      当返回 ``True``, 非白名单上的地址禁止交易Stoken


   burningMode
      **销毁模式** 是否打开

      ``True`` 代表 **打开**, and ``False`` for **关闭**

      当返回 ``True``, Stoken每次交易会销毁**1%**。


   burningPermill
      当 **销毁模式** 打开, 这个值才有效
      这代表每次交易销毁率

      返回 ``10`` 代表每次销毁**1%**.


在Stoken中查询某地址
----------------------------

方法 #1: **queryAccount**

.. image:: /_static/contract/stoken2_query1.png
   :width: 80 %
   :align: center
   :alt: stoken2_query1.png

输入以太坊地址，点击 **Query**按钮, then:

.. image:: /_static/contract/stoken2_query2.png
   :width: 80 %
   :align: center
   :alt: stoken2_query2.png

让我们关注返回值:

.. code-block:: text

   whitelisted               bool :     true
   whitelistReferralsCount   uint256 :  25
   balance                   uint256 :  118448326
   reserved                  uint256 :  59224163


.. NOTE::

   whitelisted
       如果返回值是 ``true``, 代表地址已经在白名单中, ``false`` 代表没有。


   whitelistReferralsCount
      直接推荐数。


   balance
      Stoken的数量, 保留6位小数
      ``118448326`` 代表 **118.448326 Stoken**。


   reserved
      Stoken剩余的数量, 保留6位小数
      ``59224163`` 代表 **59.224163 Stoken**.
