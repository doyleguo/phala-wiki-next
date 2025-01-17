---
title: "Error Summary"
weight: 1010
menu:
  compute:
    parent: "basic-info"
---

## Mining

### Worker

| Error name | Meaning | Solution |
| --- | --- | --- |
| WorkerNotRegistered | The worker is not registered in the registry when adding to the pool | Check the synchronization process and mining status of the worker |
| BenchmarkMissing | The worker doesn't have a valid benchmark when adding to the pool | Make sure the worker is mining and wait for the benchmark uploaded |
| WorkerDoesNotExist | The worker is already added to the pool | - |
| WorkerInAnotherPool | The worker is already added to another pool | Remove it from the pool to which the worker is added before if it's not the pool you want to add the worker to |
| UnauthorizedOperator | The access to a worker is granted by its operator parameter set by register_worker | Check the config on the mining scripts |
| InsufficientFreeStake | Cannot start mining because there's no enough free stake | The stake amount you set to the work is more than the free stake amount in the pool. Set a number that is less than the free stake or delegates more PHA in the pool |
| WorkersExceedLimit | Failed to add a worker because the number of the workers exceeds the upper limit. | Create another pool or remove the useless worker in this pool (Make sure the worker is stopped and reclaimed before you remove it) |
| CannotRestartWithLessStake | Restarted with a less stake is not allowed in the tokenomic. | - |
| MinerNotReady | Miner is not in Ready state to proceed. | Wait for a 7 days period of Cool-down and reclaim it when the period is finished |
| MinerNotMining | Miner is not in Mining state to stop mining. | - |
| CoolDownNotReady | Cannot reclaim the worker because it's still in cooldown period. | Wait for the 7 days period of Cool-down and reclaim it when the period is finished |
| TooMuchStake | Cannot start mining because there's too much stake (exceeds Vmax). | The stake amount you set for the worker is more than the maximum stake amount of the worker. Set a lower number and try again. How to calculate the maximum stake: Phala Tokenomics |
| BenchmarkTooLow | Indicating the initial benchmark score is too low to start mining. | Make sure your worker has a high-quality computing power. Restart your mining scripts and check the mining score on the mining status. If the mining score is still under 100, the worker will not be allowed to participate the Phala Mining. |
| MinerNotFound | Miner not found. | - |
| MinerNotBound | Not permitted because the miner is not bound with a worker. | - |
| WorkerNotBound | Not permitted because the worker is not bound with a miner account. | - |
| InternalErrorBadTokenomicParameters | Internal error. The tokenomic parameter is not set. | Please contact the Phala Team the bug you meet, thank you |

### Pool

| Error name | Meaning	 | Solution |
| --- | --- | --- |
| InadequateCapacity | The stake capacity is set too low to cover the existing stake | Set a higher cap that is not less than the amount of existing delegation |
| NoRewardToClaim | There's no pending reward to claim | Keep patient and learn about the Principles of payment events |
| AlreadyInContributeWhitelist | Can not add the staker to whitelist because the staker is already in whitelist. | - |
| ExceedWhitelistMaxLen | Too many stakers in contribution whitelist that exceed the limit | remove the useless whitelist in this pool |


## Delegate


| Error name | Meaning	 | Solution |
| --- | --- | --- |
| StakeExceedsCapacity | The stake added to a pool exceeds its capacity | You can't add the delegation amount more than the delegatable amount of the pool |
| InsufficientContribution | The contributed stake is smaller than the minimum threshold | Set a delegation amount that is more than 0.01 PHA |
| InsufficientBalance | Trying to contribute more than the available balance | You don't have enough transferrable balance. Check your transferrable balance |
| InvalidWithdrawalAmount | The withdrawal amount is too small (considered as dust) | The withdrawal amount should be more than 0.01 PHA |
| NoRewardToClaim | There's no pending reward to claim | Keep patient and learn about the Principles of payment events |
| NotInContributeWhitelist | Invalid staker to contribute because origin isn't in Pool's contribution whitelist. | Ask the pool owner to add you to the whitelist |
