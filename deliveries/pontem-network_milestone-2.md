# Milestone Delivery :mailbox:

**The [invoice form :pencil:](https://forms.gle/8Wx7nxtq8fKrsuEz8) has been filled out correctly for this milestone and the delivery is according to the official [milestone delivery guidelines](https://github.com/w3f/General-Grants-Program/blob/master/grants/milestone-deliverables-guidelines.md).**  

* **PR Link:** [Pontem Network](https://github.com/w3f/Open-Grants-Program/pull/138). 
* **Milestone Number:** [Milestone #2](https://github.com/w3f/Open-Grants-Program/blob/master/applications/pontem.md#milestone-2--alpha-version-of-move-pallet).

See how to try result of work on milestone #2: Move VM, Move Pallet, and tools, in Move Pallet [documentation](https://github.com/pontem-network/sp-move/blob/master/README.md).

| Number | Deliverable | Link | Notes |
| ------------- | ------------- | ------------- |------------- |
| 0-1. | Adopt storage - WriteSets processing | [Move Pallet](https://github.com/pontem-network/sp-move/commit/45a2cfb4d33db5f4a5792b43de313b313d3ec3ca)  | Move Pallet saving result of transaction execution in pallet storage. We still use LCS codec instead of Polkadot one, as migration is too expensive. |
| 2. | Events processing | [Move Pallet Commit #1](https://github.com/pontem-network/sp-move/commit/45a2cfb4d33db5f4a5792b43de313b313d3ec3ca) [Move Pallet Commit #2](https://github.com/pontem-network/sp-move/commit/d74a74801bf5f6f24096ad86df929708f3c39d14) | Events generated by smart contracts are written to storage now. Their format is compatible with Diem. |
| 3. | Publish Transaction | [Move Pallet Commit #1](https://github.com/pontem-network/sp-move/commit/b96592a3b7af3cd3dbf8b5521ae4d558479f7e47) [Move Pallet](https://github.com/pontem-network/sp-move/blob/master/pallets/sp-mvm/src/lib.rs#L105) | Developers can publish their own custom modules to network and use them in other modules/scripts. |
| 4. | Execute Arguments Parsing | [Move Pallet](https://github.com/pontem-network/sp-move/commit/79acc0aafcfaa5279bd4d570cd8aa368d82ee526#diff-ca0cca5ccd74d8e068826c35fd076cac894c357c184a1cd8177a966e9d3be207) [Move Tools](https://github.com/pontem-network/move-tools/commit/fe920402fed2ce71608369dbe43ab672a2518468) [Move VM Commit #1](https://github.com/pontem-network/sp-move-vm/commit/906aa625fba6c52d8d96ea56b4e41ac16f587460) [Move VM Commit #2](https://github.com/pontem-network/sp-move-vm/commit/ad0075005369470f7a509345b456647432670905) | Move VM now supports different kinds of arguments including primitives and vectors. Developers can encode their arguments to send transactions containing VM scripts using Move Tools. See Move Tools [docs](https://github.com/pontem-network/move-tools#dove). |
| 5. | Standard Library	| [Move Pallet](https://github.com/pontem-network/sp-move/commit/d74a74801bf5f6f24096ad86df929708f3c39d14) [Standard Library](https://github.com/pontem-network/move-stdlib) | Publish Move standard library via transaction from root account. Also, the standard library variant for pallet provides an access to block height, time, balances, signatures etc. |
| 6. | Execute Transaction | [Move Pallet](https://github.com/pontem-network/sp-move/blob/master/pallets/sp-mvm/src/lib.rs#L70) [Move Pallet Commit #1](https://github.com/pontem-network/sp-move/commit/f0781c98543b1d5afc3a35f5041cb116438516c4#diff-4e5930d2e2ba9c4d86fb707cc5d1eb7aef9839019ea8e6f3125310aa710557cbR189) | Transactions containing Move script are recognized and executed now. |
| 7. | Unit-tests | [Coverage](https://coveralls.io/github/fzzr-/sp-move)  | All our repositories and projects contain tests, we always try to cover as much as possible code with tests, yet, we still need to have balance between developing and supporting (tests). By link you can see coverage of Move Pallet. |
| 8. | Resource viewer | [Move Tools Commit #1](https://github.com/pontem-network/move-tools/commit/0e17a968141489d51831ba676ae039853383b225#diff-a02b84e9844a8ab53003088e12eaf650c775f16534029532216fa1f66369954c) [Move Tools Commit #2](https://github.com/pontem-network/move-tools/commit/ec8175310ce078d19f7a779eec03fd6cf56cff7e#diff-a02b84e9844a8ab53003088e12eaf650c775f16534029532216fa1f66369954c) | Adopted Move tools for Move Pallet. See [documentation](https://github.com/pontem-network/move-tools/blob/master/resource-viewer/README.md) for details and examples. |

Some items of current milestone we finished during previous [milestone #1](/deliveries/pontem-network_milestone-1.md), like items related to storage, events processing, yet we improved some functionality during this milestone, like adopted events similar to Diem format. Same with items related to publishing modules and executing scripts.

We are going forward, not everything we worked included in this milestone, as it also bug fixes, improvements, refactorings, you can find more in our repositories:

* [Move VM](https://github.com/pontem-network/sp-move-vm)
* [Move Pallet](https://github.com/pontem-network/sp-move)
* [Move Tools](https://github.com/pontem-network/move-tools)

In the next milestone we also plan to improve documentation, up gitbook, add more examples and etc.
