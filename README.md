# A Value Internet Sharing Bitcoin’s Consensus Security

## BEVM Development Phases
The development of BEVM has undergone a deep reflection on the core design concepts of Bitcoin and Ethereum, and has gradually formed the current paradigm through multiple technical explorations.
### 1. BTC Layer2 Exploration
- **Goal**: Address Bitcoin’s limited scalability by using Layer2 solutions to improve transaction throughput.  
- **Lessons Learned**: While technically feasible, Layer2 solutions lacked strong ecological demand, meaning they did not fundamentally change Bitcoin’s usage or achieve broad adoption.  
- **White Paper**: 
  - [BTC Layer2 White Paper(English)](https://github.com/BitAgere/BitAgere_WhitePaper/blob/main/docs/BEVM_Whitepaper2023_EN.pdf) 
  - [BTC Layer2 White Paper(Chinese)](https://github.com/BitAgere/BitAgere_WhitePaper/blob/main/docs/BEVM_Whitepaper2023_CN.pdf)

### 2. Taproot Consensus
- **Innovation**: Combined Bitcoin SPV state channels with Taproot technology to enable decentralized custody and expand Bitcoin’s smart contract capabilities.  
- **Reflections**: Bitcoin (BTC) is already widely adopted as a currency in centralized exchanges and mining pools, with relatively limited demand for decentralization-based expansion. What truly requires enhancement is Bitcoin’s consensus mechanism rather than BTC’s monetary function alone.  
- **White Paper**: 
  - [Taproot Consensus White Paper(English)](https://github.com/BitAgere/BitAgere_WhitePaper/blob/main/docs/Taproot_Consensus_yellow_paper.pdf)
  - [Taproot Consensus White Paper(Chinese)](https://github.com/BitAgere/BitAgere_WhitePaper/blob/main/docs/Taproot_Consensus_CN.pdf)

### 3. SuperBitcoin
- **Direction**: Proposed a new crypto system that shares the security advantages of Bitcoin’s consensus.  
- **Limitations**: Improved consensus security but did not solve the “dreamworld disconnection” in Ethereum-like VMs. Such systems run only within their internal liquidity environment and lack the ability to perceive and interact with real-world data and states.  
- **White Paper**: 
  - [SuperBitcoin White Paper(English)](https://github.com/BitAgere/BitAgere_WhitePaper/blob/main/docs/Super_Bitcoin_Whitepaper.pdf)
  - [SuperBitcoin White Paper(Chinese)](https://github.com/BitAgere/BitAgere_WhitePaper/blob/main/docs/Super_Bitcoin_Whitepaper_CN.pdf)

### 4. BitAgere
- **Problem**: Identified parallels between Bitcoin’s mechanical consensus and AI Agents’ abstract cognition, leading to the concept of BitAgere.  
- **Innovation**: Based on SuperBitcoin, focused on solving mechanical consensus’ perception gap. AI Agents’ input-sensing capability is abstracted and connected on-chain, enabling crypto systems to have real-world perceptive power. This deep integration of Crypto and AI Agents forms the basis for BitAgere.  
- **White Paper**:  
  - [BitAgere White Paper (English)](https://github.com/BitAgere/BitAgere_WhitePaper/blob/main/docs/BitAgere_A_multi-dimensional_Agere_interconnection_system_based_on_Bitcoin.pdf)
  - [BitAgere White Paper (Chinese)](https://github.com/BitAgere/BitAgere_WhitePaper/blob/main/docs/BitAgere_一个以Bitcoin为底层的多元Agere互联系统.pdf)  

### 5. BEVM(λ) Paradigm
- **Discovery**: Through introspecting Bitcoin’s design philosophy, we formulated the BEVM(λ) paradigm. It provides systemic theoretical guidance by examining Bitcoin’s success from four core aspects: the Individual model, lambda calculus, consensus algorithm, and consensus-aware algorithm.  
- **Direction**: BEVM(λ) inherits Bitcoin’s principles of energy conservation and decentralized emergence while enhancing autonomy and intelligence. Powered by the Agere subsystem and supported by distributed stateless computation and consensus-aware algorithms, BEVM(λ) paves the way for diverse future applications and the comprehensive development of intelligent crypto systems.  
- **White Paper**:
  - [BEVM(λ) White Paper(English)](https://github.com/BitAgere/BitAgere_WhitePaper/blob/main/docs/Agere_Consensus_Intelligent_Cryptocurrency_Design_Based_on_BEVM.pdf)
  - [BEVM(λ) White Paper(Chinese)](https://github.com/BitAgere/BitAgere_WhitePaper/blob/main/docs/Agere共识_基于BEVM(λ)的智能加密货币设计.pdf)

## Abstract
Super Bitcoin is a value-based internet centered around BTC, and sharing Bitcoin's consensus security. 
This value internet not only inherits the security of the existing Bitcoin network but also transcends BTC's current limitations of being solely used for transfer, providing the Bitcoin network with unlimited scalability and flexibility.

Although the Lightning Network [2] inherits Bitcoin's network security and offers partial scalability solutions, it still falls short in supporting smart contracts and further enhancing scalability.
We propose a five-layer architecture for Super Bitcoin using the Bitcoin network as the kernel layer, maintaining system security and transaction irreversibility through the proof-of-work (PoW) consensus mechanism; building an efficient communication layer based on the Lightning Network, facilitating rapid transmission of asset information while preserving Bitcoin's decentralized nature;
we introduce the Taproot Consensus as the extension layer, abstracting Lightning Network communication and asset information to provide a standardized interface for the upper virtual machine layer;
a multi-chain layer, also known as the fusion layer, consists of multiple lightning chains secured by BTC consensus, integrating any mainstream virtual machine (VM) to achieve a "Multi-chain interconnection“ and ”multi-chain interoperability” unified by BTC consensus;
finally, at the application layer, providing developers with rich tools and interfaces to build a decentralized application (DApp) ecosystem, all sharing the security of BTC consensus.

## 1. Introduction
As the pioneer of cryptocurrencies, Bitcoin (BTC), through its proof-of-work (PoW) consensus mechanism and decentralized network structure, has garnered an immense level of consensus, becoming a supranational currency. This security stems from the perfect combination of its vast network hash power and economic incentives.
The birth of Bitcoin not only ushered in a new era of decentralized digital currency but also pointed the way for the subsequent development of blockchain technology. 
However, the limitations of Bitcoin’s scripting language soon became apparent, as it only supports simple value transfers and limited contract logic, unable to meet the demands of more complex decentralized applications.

The evolution of blockchain technology is essentially all about expanding and enhancing Bitcoin's capabilities.
Vitalik Buterin, the founder of Ethereum, initially envisioned adding smart contract functionality to Bitcoin. 
However, due to the technological constraints of the time and the limitations of the Bitcoin network, Ethereum had to establish its own independent consensus system. 
While this approach allowed for the creation of Turing-complete smart contracts, it also introduced new security risks and scalability challenges. 
Many projects followed suit, building independent blockchain ecosystems, gradually diverging from and even forgetting the original intention of extending Bitcoin’s capabilities.

However, two key factors remind us of the need to reconsider this direction. 
First, the continued rise in Bitcoin’s value relative to other cryptocurrencies like Ethereum has validated the trust people place in its security and stability. 
Second, the collapse of Luna/UST, which wiped out nearly $100 billion in market value, highlighted the severe security vulnerabilities present in independent consensus chains, especially when faced with complex economic models and rapidly growing network value.
In this context, we introduce Super Bitcoin to create a true value internet sharing Bitcoin's consensus security.
It fundamentally differs from the existing Bitcoin Layer 2 solutions: traditional Bitcoin Layer 2 solutions (such as the Lightning Network) mainly achieve fast payments through off-chain state channels and limited scripts, while sharing Bitcoin's consensus security but lacking flexibility.
Meanwhile, sidechains  like Stacks or Layer 2 solutions, although they support smart contracts, still rely on independent multi-signature mechanisms for security, thus not fully inheriting the security of the Bitcoin mainnet.


## 3. System Architecture
![image](https://github.com/user-attachments/assets/04785c9a-0665-483f-a892-b257f4aec2d9)

### 3.1 System Architecture Overview
Super Bitcoin is a five-layer architecture protocol built by BEVM guided by the three problems of blockchain - decentralization, security and scalability.
This protocol is based on the Bitcoin protocol and utilizes the Lightning Network for efficient peer-to-peer communication. 
To extend the functionality of Lightning Network nodes, Super Bitcoin integrates Taproot Consensus and combines Bitcoin SPV, Schnorr signatures, MAST contracts, and a BFT PoS consensus mechanism to achieve scalable state management and transaction processing.
On this foundation, Super Bitcoin further integrates multiple virtual machines, including WASM, EVM, SVM, MoveVM, and CairoVM, creating a multi-chain system based on lightning chains that offer a diverse range of smart contract execution environments.
This modular framework significantly enhances the system's scalability and flexibility while maintaining the decentralized nature of the Bitcoin network. 
Importantly, all lightning chains share the Bitcoin network's consensus security, ensuring that the system remains highly secure as it scales.


## For more details, please see the [Super Bitcoin white paper](https://github.com/btclayer2/SuperBitcoin/blob/main/Super%20Bitcoin%20Whitepaper.pdf)
## 更多细节，请看[Super Bitcoin 中文白皮书](https://github.com/btclayer2/SuperBitcoin/blob/main/Super%20Bitcoin%20%E4%B8%AD%E6%96%87%E7%99%BD%E7%9A%AE%E4%B9%A6.pdf)
