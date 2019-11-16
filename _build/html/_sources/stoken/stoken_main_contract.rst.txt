.. _stoken2_main_contract:

Stoken主合约
=======================

这是 :ref:`stoken` 的**核心合约**,最后更新于 ``2019-10-02 16:12:41 UTC``.

|logo_etherscan_verified| |logo_github| |logo_verified|

- 合约地址是**0x460cbb9409a024a55f2b7b7f69afd0da385ce850**
- 部署于`Tx Hash 0x92f717e0385ec5505aac0e3a093c1f03e2bdffbb4a48d620a62cc80735ff1c83`_
- 区块号`#8623851`_
- 开源在`GNU General Public License v3.0`_协议下
- `在github仓库中查看合约代码`_

在Etherscan.io上查看:

- `Stoken交易追踪`_
- `查看合约的交易和动向`_
- `在Etherscan.io中查看合约`_
- `在Etherscan.io中编写合约`_

.. _Tx Hash 0x92f717e0385ec5505aac0e3a093c1f03e2bdffbb4a48d620a62cc80735ff1c83:
   https://etherscan.io/tx/0x92f717e0385ec5505aac0e3a093c1f03e2bdffbb4a48d620a62cc80735ff1c83
.. _#8623851:
   https://etherscan.io/block/8623851
.. _GNU General Public License v3.0:
   https://github.com/beyoubox/contracts/LICENSE
.. _在github仓库中查看合约代码:
   https://github.com/beyoubox/contracts/BeyouCoin.sol
.. _Stoken交易追踪:
   https://etherscan.io/token/0x460cbb9409a024a55f2b7b7f69afd0da385ce850
.. _查看合约的交易和动向:
   https://etherscan.io/address/0x460cbb9409a024a55f2b7b7f69afd0da385ce850
.. _在Etherscan.io中查看合约:
   https://etherscan.io/address/0x460cbb9409a024a55f2b7b7f69afd0da385ce850#readContract
.. _在Etherscan.io中编写合约:
   https://etherscan.io/address/0x460cbb9409a024a55f2b7b7f69afd0da385ce850#writeContract


.. |logo_github| image:: /_static/logos/github.svg
   :width: 36px
   :height: 36px

.. |logo_etherscan_verified| image:: /_static/logos/etherscan_verified.svg
   :width: 36px
   :height: 36px

.. |logo_verified| image:: /_static/logos/verified.svg
   :width: 36px
   :height: 36px


``Stoken``
-----------------------------------

在一些钱包软件，例如`MetaMask`_,
`MyEtherWallet`_, `imToken`_, `etherscan.io`_ 和以太坊区块浏览器.

.. _MetaMask: https://metamask.io/
.. _MyEtherWallet: https://www.myetherwallet.com/
.. _imToken: https://imkey.im/
.. _etherscan.io: https://etherscan.io/


特点与功能
----------------------

.. _stoken_based_on_erc20:

基于 `[EIP 20] ERC-20 货币标准`_ of `Ethereum`_
   Includes:

   - ``function name() public view returns (string)``
   - ``function symbol() public view returns (string)``
   - ``function decimals() public view returns (uint8)``
   - ``function totalSupply() public view returns (uint256)``
   - ``function balanceOf(address account) public view returns (uint256)``
   - ``function transfer(address recipient, uint256 amount) public returns (bool)``
   - ``function transferFrom(address sender, address recipient, uint256 amount) public returns (bool)``
   - ``function approve(address spender, uint256 value) public returns (bool)``
   - ``function allowance(address owner, address spender) public view returns (uint256)``
   - ``event Transfer(address indexed from, address indexed to, uint256 value)``
   - ``event Approval(address indexed owner, address indexed spender, uint256 value)``

   With advanced functions for allowance:

   - ``function increaseSupply(address spender, uint256 addedValue) public returns (bool)``
   - ``function decreaseSupply(address spender, uint256 subtractedValue) public returns (bool)``


.. _[EIP 20] ERC-20 货币标准: https://eips.ethereum.org/EIPS/eip-20
.. _Ethereum: https://www.ethereum.org


.. _stoken_supports_freezing:

支持灵活的**锁仓**功能
   锁仓方法:

   - ``function lock(address _addr, uint256 _value) external returns (uint256)``

   取消锁仓方法:

   - ``function unlock(address _addr, uint256 _value) public returns (uint256)``
