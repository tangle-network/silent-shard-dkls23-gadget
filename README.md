# silent-shard-dkls23-gadget

This repo implements the Silence Laboratories DKLS protocol into Tangle's [gadget](https://github.com/webb-tools/gadget). The DKLS protocol is a distributed key generation protocol that allows a group of parties to generate a group ECDSA public key and a set of secret key shares for each participant. A threshold number of parties can then collaborate to sign a message using the group key. The protocol is secure against malicious adversaries and can be used in a variety of applications such as secure multi-party computation, threshold signatures, and secure messaging.

The gadget integration allows this protocol to be used against the Tangle blockchain. Tangle implements a job management system that allows users to submit jobs to the network and receive results. The test framework contained within this gadget implementation interacts with a mock Tangle blockchain to ensure that the DKLS protocol is functioning correctly and the results are as expected.

## Getting Started
This project represents a single protocol implementation on top of Tangle's [gadget](https://github.com/webb-tools/gadget) framework. We recommend checking out https://github.com/webb-tools/gadget for more information on how to use the framework and how to build your own protocol implementations.

### Prerequisites

- Rust 1.74.0 or higher
- Substrate blockchain with compatible job management and submission infrastructure

### Installation

1. Clone the repository:

```bash
git clone https://github.com/webb-tools/silent-shard-dkls23-gadget/
cd silent-shard-dkls23-gadget
```
   
2. Build the project:

```bash
cargo build --release
```

3. Run the tests:

```bash
RUST_LOG=gadget=trace cargo nextest run -r
```

## Acknowledgements
We would like to thank the following projects for their inspiration and contributions to this repository:

* [DKLS](https://github.com/silence-laboratories/silent-shard-dkls23-ll)