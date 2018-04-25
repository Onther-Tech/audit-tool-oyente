# audit-tool-oyente

[oyente](https://github.com/melonproject/oyente) is analysis tool for smart contracts

## Quick start

to open the container, install docker and run:
```bash
docker pull luongnguyen/oyente && docker run -i -t luongnguyen/oyente
```

change directory:
```bash
cd oyente
```

get solidity file for testing
```bash
git clone https://github.com/Onther-Tech/tokyo.git
```

run:
```bash
python oyente.py -s tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/AuditFullFeaturesCrowdsale.sol
```

log from [this commit](https://github.com/Onther-Tech/tokyo/commit/a6c46b6939a21bb0138284cfbd02d8a353fb2446):
```bash
WARNING:root:You are using evm version 1.8.2. The supported version is 1.7.3
WARNING:root:You are using solc version 0.4.21, The latest supported version is 0.4.19
INFO:root:contract tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/AuditFullFeaturesCrowdsale.sol:AuditFullFeaturesCrowdsale:
INFO:symExec:	============ Results ===========
INFO:symExec:	  EVM Code Coverage: 			 49.5%
INFO:symExec:	  Integer Underflow: 			 True
INFO:symExec:	  Integer Overflow: 			 True
INFO:symExec:	  Parity Multisig Bug 2: 		 False
INFO:symExec:	  Callstack Depth Attack Vulnerability:  False
INFO:symExec:	  Transaction-Ordering Dependence (TOD): False
INFO:symExec:	  Timestamp Dependency: 		 False
INFO:symExec:	  Re-Entrancy Vulnerability: 		 False
INFO:symExec:tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/AuditFullFeaturesCrowdsale.sol:86:5: Warning: Integer Underflow.
    locker = Locker(_l
INFO:symExec:tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/AuditFullFeaturesCrowdsale.sol:52:3: Warning: Integer Overflow.
  function init(bytes32[] args) public {
  ^
Spanning multiple lines.
Integer Overflow occurs if:
    args = 115792089237316195423570985008687907853269984665640564039457584007913129639935
tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/AuditFullFeaturesCrowdsale.sol:16:52: Warning: Integer Overflow.
  // constructor parameters are left padded bytes32.
  ^
Spanning multiple lines.
tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/AuditFullFeaturesCrowdsale.sol:47:43: Warning: Integer Overflow.
  function generateHoldersTokens(uint256 _targetTotalSupply) internal {
  ^
Spanning multiple lines.
tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/AuditFullFeaturesCrowdsale.sol:25:8: Warning: Integer Overflow.
    MinimumPaymentCrowdsale(
    ^
Spanning multiple lines.
INFO:symExec:	====== Analysis Completed ======
INFO:root:contract tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/common/HolderBase.sol:HolderBase:
INFO:symExec:	============ Results ===========
INFO:symExec:	  EVM Code Coverage: 			 50.6%
INFO:symExec:	  Integer Underflow: 			 False
INFO:symExec:	  Integer Overflow: 			 True
INFO:symExec:	  Parity Multisig Bug 2: 		 False
INFO:symExec:	  Callstack Depth Attack Vulnerability:  False
INFO:symExec:	  Transaction-Ordering Dependence (TOD): False
INFO:symExec:	  Timestamp Dependency: 		 False
INFO:symExec:	  Re-Entrancy Vulnerability: 		 False
INFO:symExec:tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/common/HolderBase.sol:35:3: Warning: Integer Overflow.
  function initHolders(address[] _addrs, uint96[] _ratios) public onlyOwner {
  ^
Spanning multiple lines.
Integer Overflow occurs if:
    _addrs = 115792089237316195423570985008687907853269984665640564039457584007913129639935
INFO:symExec:	====== Analysis Completed ======
INFO:root:contract tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/kyc/KYC.sol:KYC:
INFO:symExec:	============ Results ===========
INFO:symExec:	  EVM Code Coverage: 			 66.3%
INFO:symExec:	  Integer Underflow: 			 False
INFO:symExec:	  Integer Overflow: 			 True
INFO:symExec:	  Parity Multisig Bug 2: 		 False
INFO:symExec:	  Callstack Depth Attack Vulnerability:  False
INFO:symExec:	  Transaction-Ordering Dependence (TOD): False
INFO:symExec:	  Timestamp Dependency: 		 False
INFO:symExec:	  Re-Entrancy Vulnerability: 		 False
INFO:symExec:tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/kyc/KYC.sol:67:3: Warning: Integer Overflow.
  function registerByList(address[] _addrs)
  ^
Spanning multiple lines.
tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/kyc/KYC.sol:97:3: Warning: Integer Overflow.
  function unregisterByList(address[] _addrs)
  ^
Spanning multiple lines.
INFO:symExec:	====== Analysis Completed ======
INFO:root:contract tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/locker/Locker.sol:Locker:
INFO:symExec:	============ Results ===========
INFO:symExec:	  EVM Code Coverage: 			 50.9%
INFO:symExec:	  Integer Underflow: 			 True
INFO:symExec:	  Integer Overflow: 			 True
INFO:symExec:	  Parity Multisig Bug 2: 		 False
INFO:symExec:	  Callstack Depth Attack Vulnerability:  False
INFO:symExec:	  Transaction-Ordering Dependence (TOD): False
INFO:symExec:	  Timestamp Dependency: 		 False
INFO:symExec:	  Re-Entrancy Vulnerability: 		 False
INFO:symExec:tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/locker/Locker.sol:196:28: Warning: Integer Underflow.
    require(_releaseRatios[len - 1
Integer Underflow occurs if:
    state = 0
    locked[_beneficiary] = 0
    beneficiaries[_addr].ratio = 115792089237316195423570985008687907853269984665640564039457584007913129639935
INFO:symExec:tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/locker/Locker.sol:168:12: Warning: Integer Overflow.
    return releases[_beneficiary].releaseTimes
Integer Overflow occurs if:
    beneficiaries[_addr].ratio = 115792089237316195423570985008687907853269984665640564039457584007913129639935
tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/locker/Locker.sol:177:12: Warning: Integer Overflow.
    return releases[_beneficiary].releaseRatios
Integer Overflow occurs if:
    beneficiaries[_addr].ratio = 115792089237316195423570985008687907853269984665640564039457584007913129639935
INFO:symExec:	====== Analysis Completed ======
INFO:root:contract tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/minime/Controlled.sol:Controlled:
INFO:symExec:	============ Results ===========
INFO:symExec:	  EVM Code Coverage: 			 99.4%
INFO:symExec:	  Integer Underflow: 			 False
INFO:symExec:	  Integer Overflow: 			 False
INFO:symExec:	  Parity Multisig Bug 2: 		 False
INFO:symExec:	  Callstack Depth Attack Vulnerability:  False
INFO:symExec:	  Transaction-Ordering Dependence (TOD): False
INFO:symExec:	  Timestamp Dependency: 		 False
INFO:symExec:	  Re-Entrancy Vulnerability: 		 False
INFO:symExec:	====== Analysis Completed ======
INFO:root:contract tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/minime/MiniMeToken.sol:MiniMeToken:
INFO:symExec:	============ Results ===========
INFO:symExec:	  EVM Code Coverage: 			 54.1%
INFO:symExec:	  Integer Underflow: 			 True
INFO:symExec:	  Integer Overflow: 			 True
INFO:symExec:	  Parity Multisig Bug 2: 		 False
INFO:symExec:	  Callstack Depth Attack Vulnerability:  False
INFO:symExec:	  Transaction-Ordering Dependence (TOD): False
INFO:symExec:	  Timestamp Dependency: 		 False
INFO:symExec:	  Re-Entrancy Vulnerability: 		 False
INFO:symExec:tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/minime/MiniMeToken.sol:40:5: Warning: Integer Underflow.
    string public name
tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/minime/MiniMeToken.sol:42:5: Warning: Integer Underflow.
    string public symbol
tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/minime/MiniMeToken.sol:43:5: Warning: Integer Underflow.
    string public version = 'MMT_0.2'
INFO:symExec:tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/minime/MiniMeToken.sol:459:51: Warning: Integer Overflow.
               Checkpoint storage oldCheckPoint = checkpoints[checkpoints.length-1]
Integer Overflow occurs if:
    balances[_owner].length = 115792089237316195423570985008687907853269984665640564039457584007913129639933
    balances[_owner][0].fromBlock = 0
    parentSnapShotBlock = 1180591620717411303423
    controller = 1461501637330902918203684832716283019655932542975
tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/minime/MiniMeToken.sol:344:5: Warning: Integer Overflow.
    function createCloneToken(
    ^
Spanning multiple lines.
tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/minime/MiniMeToken.sol:454:13: Warning: Integer Overflow.
        || (checkpoints[checkpoints.length -1]
Integer Overflow occurs if:
    balances[_owner].length = 2
    balances[_owner][0].fromBlock = 115792089233946202090177155034354530967392530831435920986640012447775178358784
    parentSnapShotBlock = 170141183460469231731687286123698061309
    controller = 1461501637330902918203684832716283019655932542975
tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/minime/MiniMeToken.sol:254:5: Warning: Integer Overflow.
    function approveAndCall(address _spender, uint256 _amount, bytes _extraData
    ^
Spanning multiple lines.
INFO:symExec:	====== Analysis Completed ======
INFO:root:contract tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/minime/MiniMeToken.sol:MiniMeTokenFactory:
INFO:symExec:	============ Results ===========
INFO:symExec:	  EVM Code Coverage: 			 1.2%
INFO:symExec:	  Integer Underflow: 			 False
INFO:symExec:	  Integer Overflow: 			 True
INFO:symExec:	  Parity Multisig Bug 2: 		 False
INFO:symExec:	  Callstack Depth Attack Vulnerability:  False
INFO:symExec:	  Transaction-Ordering Dependence (TOD): False
INFO:symExec:	  Timestamp Dependency: 		 False
INFO:symExec:	  Re-Entrancy Vulnerability: 		 False
INFO:symExec:tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/minime/MiniMeToken.sol:543:5: Warning: Integer Overflow.
    function createCloneToken(
    ^
Spanning multiple lines.
Integer Overflow occurs if:
    _tokenName = 115792089237316195423570985008687907853269984665640564039457584007913129639932
INFO:symExec:	====== Analysis Completed ======
INFO:root:contract tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/vault/MultiHolderVault.sol:MultiHolderVault:
INFO:symExec:	============ Results ===========
INFO:symExec:	  EVM Code Coverage: 			 75.5%
INFO:symExec:	  Integer Underflow: 			 False
INFO:symExec:	  Integer Overflow: 			 True
INFO:symExec:	  Parity Multisig Bug 2: 		 False
INFO:symExec:	  Callstack Depth Attack Vulnerability:  False
INFO:symExec:	  Transaction-Ordering Dependence (TOD): True
INFO:symExec:	  Timestamp Dependency: 		 False
INFO:symExec:	  Re-Entrancy Vulnerability: 		 False
INFO:symExec:tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/vault/MultiHolderVault.sol:27:72: Warning: Integer Overflow.

tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/vault/MultiHolderVault.sol:27:393: Warning: Integer Overflow.

INFO:symExec:Flow1
Flow2
INFO:symExec:	====== Analysis Completed ======
INFO:root:contract tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/zeppelin/crowdsale/RefundVault.sol:RefundVault:
INFO:symExec:	============ Results ===========
INFO:symExec:	  EVM Code Coverage: 			 98.7%
INFO:symExec:	  Integer Underflow: 			 False
INFO:symExec:	  Integer Overflow: 			 True
INFO:symExec:	  Parity Multisig Bug 2: 		 False
INFO:symExec:	  Callstack Depth Attack Vulnerability:  False
INFO:symExec:	  Transaction-Ordering Dependence (TOD): True
INFO:symExec:	  Timestamp Dependency: 		 False
INFO:symExec:	  Re-Entrancy Vulnerability: 		 False
INFO:symExec:tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/zeppelin/crowdsale/RefundVault.sol:44:11: Warning: Integer Overflow.
  function enab
Integer Overflow occurs if:
    state = 0
    deposited[investor] = 1
INFO:symExec:Flow1
tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/zeppelin/crowdsale/RefundVault.sol:41:5: Warning: Transaction-Ordering Dependency.
    wallet.transfer(this.balance)
Flow2
tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/zeppelin/crowdsale/RefundVault.sol:54:5: Warning: Transaction-Ordering Dependency.
    investor.transfer(depositedValue)
INFO:symExec:	====== Analysis Completed ======
INFO:root:contract tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/zeppelin/math/SafeMath.sol:SafeMath:
INFO:symExec:	============ Results ===========
INFO:symExec:	  EVM Code Coverage: 			 100.0%
INFO:symExec:	  Integer Underflow: 			 False
INFO:symExec:	  Integer Overflow: 			 False
INFO:symExec:	  Parity Multisig Bug 2: 		 False
INFO:symExec:	  Callstack Depth Attack Vulnerability:  False
INFO:symExec:	  Transaction-Ordering Dependence (TOD): False
INFO:symExec:	  Timestamp Dependency: 		 False
INFO:symExec:	  Re-Entrancy Vulnerability: 		 False
INFO:symExec:	====== Analysis Completed ======
INFO:root:contract tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/zeppelin/ownership/Ownable.sol:Ownable:
INFO:symExec:	============ Results ===========
INFO:symExec:	  EVM Code Coverage: 			 99.5%
INFO:symExec:	  Integer Underflow: 			 False
INFO:symExec:	  Integer Overflow: 			 False
INFO:symExec:	  Parity Multisig Bug 2: 		 False
INFO:symExec:	  Callstack Depth Attack Vulnerability:  False
INFO:symExec:	  Transaction-Ordering Dependence (TOD): False
INFO:symExec:	  Timestamp Dependency: 		 False
INFO:symExec:	  Re-Entrancy Vulnerability: 		 False
INFO:symExec:	====== Analysis Completed ======
INFO:root:contract tokyo/packages/tokyo-reusable-crowdsale/audit/full-features/contracts/base/zeppelin/token/ERC20/SafeERC20.sol:SafeERC20:
INFO:symExec:	============ Results ===========
INFO:symExec:	  EVM Code Coverage: 			 100.0%
INFO:symExec:	  Integer Underflow: 			 False
INFO:symExec:	  Integer Overflow: 			 False
INFO:symExec:	  Parity Multisig Bug 2: 		 False
INFO:symExec:	  Callstack Depth Attack Vulnerability:  False
INFO:symExec:	  Transaction-Ordering Dependence (TOD): False
INFO:symExec:	  Timestamp Dependency: 		 False
INFO:symExec:	  Re-Entrancy Vulnerability: 		 False
INFO:symExec:	====== Analysis Completed ======
```
