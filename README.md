# Merkle Airdrop Starter

Quickly bootstrap an ERC20 token airdrop to a Merkle tree of recipients.

Steps:

1. Generate Merkle tree of recipients by following README in [generator/](https://github.com/Anish-Agnihotri/merkle-airdrop-starter/tree/master/generator)
2. Setup and deploy MerkleClaimERC20 contracts by following README in [contracts/](https://github.com/Anish-Agnihotri/merkle-airdrop-starter/tree/master/contracts)
3. Setup and deploy front-end by following README in [frontend/](https://github.com/Anish-Agnihotri/merkle-airdrop-starter/tree/master/frontend)

## Similar work and credits

- [Astrodrop](https://astrodrop.xyz/)—Simpler way to spin up a airdrop with claim page, given existing token
- [Uniswap Merkle Distributor](https://github.com/Uniswap/merkle-distributor)—Uniswap's merkle distribution smart contracts

## License

[GNU Affero GPL v3.0](https://github.com/Anish-Agnihotri/merkle-airdrop-starter/blob/master/LICENSE)

## Disclaimer

_These smart contracts are being provided as is. No guarantee, representation or warranty is being made, express or implied, as to the safety or correctness of the user interface or the smart contracts. They have not been audited and as such there can be no assurance they will work as intended, and users may experience delays, failures, errors, omissions or loss of transmitted information. Anish Agnihotri is not liable for any of the foregoing. Users should proceed with caution and use at their own risk._

## Hash function

A function that maps a bit string of arbitrary length to a fixed-length bit string. Depending upon the relying application, the security strength that can be supported by a hash function is typically measured by the extent to which it possesses one or more of the following properties

1. (Collision resistance) It is computationally infeasible to find any two distinct inputs that map to the same output.

2. (Preimage resistance) Given a randomly chosen target output, it is computationally infeasible to find any input that maps to that output. (This property is called the one-way property.)

3. (Second preimage resistance) Given one input value, it is computationally infeasible to find a second (distinct) input value that maps to the same output as the first value.

## Merkel Tree

A Merkle tree is fundamentally just a hierarchical set of hash values, building from a set of actual data (Merkle leaf) to intermediate hashes (Merkle braches) and up to the Merkle root that summarizes all the data in one hash value.

![Merkle Tree](https://raw.githubusercontent.com/BerlinP/merkle-airdrop-starter/master/assets/1_1e-wyMbvf8-u7Le1LUxTBA.webp?raw=true "A very small merkle tree")

In this figure, the bottom nodes (Data1-Data4) are the actual data processed by the application. Each of these is summarized by their respective hash value (Hash1-Hash4), as a Merkle leaf. From these, the Merkle tree builds a hierarchy, combining hashes together until only one is left. The nodes combining other hash nodes are called Merkle branches (here Hash12 and Hash34). When there is only one left (here Hash1234), this is called the Merkle root. There can be multiple levels of branches and hashing as following examples will demonstrate.

### Verify data

![Merkle Tree](https://raw.githubusercontent.com/BerlinP/merkle-airdrop-starter/master/assets/1_OA8k6-6HvA_4GJm1o6JrKQ.webp?raw=true "Verify block data")

### Use Cases

- AWS DynamoDB distributed database
- ZFS filesystem
- Git version control system

#### Blockchain use cases

- Transaction Data (Block) Immutability
- Blockchain pruning
- Simplified Payment Verification (SPV)
- Pool Mining: The Stratum Protocol
- Airdrop

## References

- [Merkle Trees: Concepts and Use Cases](https://medium.com/coinmonks/merkle-trees-concepts-and-use-cases-5da873702318)
- [Wikipedia: Merkle tree](https://en.wikipedia.org/wiki/Merkle_tree)
- [Cryptographic hash function](https://csrc.nist.gov/glossary/term/cryptographic_hash_function#:~:text=Approved%20hash%20functions%20satisfy%20the,map%20to%20the%20same%20output.)
