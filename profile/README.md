# Rhiannon AI, LLC

We're a small startup who believes privacy and cloud compute don't have to be at odds with one another - and no, the answer isn't Trusted Compute, or even Confidential Compute. [Homomorphic encryption](https://en.wikipedia.org/wiki/Homomorphic_encryption) is the answer to a large variety of problems that are centered around needing the compute power of fast machines in the cloud, to perform useful operations on public data, your own data, or data from 3rd party data provider (multi-key FHE, aka MK-FHE). At its heart, it is a collection of techniques, schemes, encoding methods, and algorithms, that enable performing nearly arbitrary compute operations on ciphertext sent to you by a client, and being able to return an encrypted ciphertext back to the user, that simultaneously retains these two properties:
1. The results are decryptable only with the same key used to encrypt the inputs and are never sent to the server
2. The operations performed on the ciphertext have to maintain enough of the 'structure' established by the encryption process (called noise in most FHE schemes) while preserving the 1st requirement.

Its not a silver bullet - we use and/or are investigating a variety of hardware accelerants:

| Accelerator                     | Accelerator Type             | Manufacturer      |
| ------------------------------- | ---------------------------- | ----------------- |
| LPDDR5X-PIM                     | Computational-RAM            | Samsung, Micron   |
| Alveo v80                       | System-on-Module/FPGA        | AMD               |
| Nvidia RTX Pro 6000             | GPU                          | Nvidia            |
| Nvidia GB300                    | Datacenter GPU Cluster       | Nvidia            |
| AI 100 Ultra                    | GPU                          | Qualcomm          |
| Quantum-Mechanical Accelerators | Quantum Mechanics            | Various Partners  |
| Photonic FHE Accelerator Cards  | Photonics                    | Various Partners  |

Photonic chips in particular show the most promise in getting to the "holy grail" of AI (and arguably, Cryptography) - mutually oblivious AI inference. Clients learn nothing about the weights - the AI models learn nothing about the requests or responses. The service provider can be anyone, since its a zero-trust model regardless.

## What is Possible Today

Small neural networks, single layers of an LLM transformer architecutre, SQL-subsett databases, facial recognition, emotion/sentiment analysis, and encrypted RAG / vector search.  Most of these algorithms can be performed fast ehough to be used in practical applications (see [Microsoft's Password Leak Detection](https://www.microsoft.com/en-us/research/blog/password-monitor-safeguarding-passwords-in-microsoft-edge/), and [Apple's Private Intelligence Caller Id Lookup](https://developer.apple.com/documentation/identitylookup/understanding-how-live-caller-id-lookup-preserves-privacy).). These are partial homomorphic scemes, which means they have a limited budget of operations they can perform before they lose the 'structure' in the ciphertext, and it becomes garbled gibberish.

## Other Useful Tools

FHE can sometimes be accelerated by limiting its application and using other primitive cryptographical operations where possible, such as [Oblivious RAM](https://en.wikipedia.org/wiki/Oblivious_RAM), [searchable encryption techniques](https://en.wikipedia.org/wiki/Searchable_symmetric_encryption) (already available in usable, Postgres-compatible products [CipherStash](https://cipherstash.com/docs/concepts/searchable-encryption)).

In addition, tradeoffs involving what exactly is encrypted and what can be in plaintext, can bring FHE into the feasbility realm today.

## What are we offering

We believe ourselves to be the first to offer a scalable, fully homomorphic and privacy-preserving encrypted vector search product. While we set up a self-service signup portal, if you're interested, we are capable of deploying a production system for you merely days after first contact. Contact us now at contact@rhiannon.biz, and learn more at our website or our free, no-signup-required, 60hr [interactive educational course](https://rhiannon.education) with audio, video, text, and interactive demonstrations to get you up to speed on chip design, the mathematics involved, managing the noise budget, and putting it all together for a useful product.
