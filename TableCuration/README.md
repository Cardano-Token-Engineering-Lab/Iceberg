# Iceberg Data Model

One of the critical pieces that will drive adoption of a data tool like Iceberg will be to ensure that the correct level and care is designed around which datasets and tables are exposed on the platform. The strategy behind the data for Iceberg will be composed of three flavors of data.  Labeling will be a critical piece to help put context to the onchain information and leveraging the cardano token registry and Cardano Fans Offchain Data Registry.  The below set of tables are goals for the project and will be evergreen as user feedback is incorporated to steer and high grade development efforts.

## **Raw Datasets**

The concept about including raw data tables is based on a couple of different ideologies.  The first is primarily to allow those with deep understanding of the Cardano blockchain to formulate and build their own connections from the most primitive forms of data that is supplied by the Cardano node.  In addition, this data can also be used to help verify some of the transformed and manipulated datasets that will come from curated data.  Lastly, in the event of limitations in encoding/decoding libraries and/or blocks/transactions that pose difficulties the raw dataset will be perserved and be used to help identify challenges that may need to be overcome

## **CNT/UTXO Tracking**

The nature of the Cardano Blockchain and it's use of the eUTXO model makes asset tracking a little more nuanced compared to account-based blockchain models. For this reason, asset tracking will be divided into two different shades where assets are matched and tracked along with UTXOs as well as matching the assets to payment and/or stake address holder of a UTXO for a particular asset.  Usage of the policy ID will be key in helping differentiating between different Cardano Native Tokens (CNTs).

   1. ***Token Transfers*** - Detailing events where assets are transferred between accounts
   2. ***Balances*** - The balances will detail the current state of a given account and the assets/UTXOs that are held by them.
   3. ***NFT Transfers*** - Although NFTs in terms of CNTs are just a variation, NFT transfers will be partitioned into it's own view to make for easy visibility of NFT assets
   4. ***Token Metadata*** - Enable views that expose metadata connected to CNTs and NFTs for users

## **DEX Data**

A very important nature of cryptocurrencies and the numerous amount of tokens that are utilized by them is understand how tokens are swapped on decentralized exchanges.  This can help with understanding behaviors of users, token valuation relative to trading pairs strength, as well as where the bulk of on-chain liquidity exists.

   1. ***DEX Trades*** - Collating individual trades on Minswap, Sundaeswap, Splash, Wingriders and more.
   2. ***DEX Prices*** - Utilizing DEX data feeds where available, enabling price feeds to the plaform and to highlight arbitrage opportunities  
   3. ***Aggregator Trades*** - Combining trades that were effectively done through aggregator platforms such as DexHunters and Steelswap
   4. ***High Value Trades*** - For raising awareness when whales transfer/exchange large values of assets onchain

## **NFT Data**

As NFTs grow beyond PFPs and start to incur additional functionality NFT data will be available for both digital collectibles and working/function-based NFTs in the Cardano Ecosystem.

   1. ***NFT Trades*** - Highlight trades done on marketplaces like jpg.store and Cardano.art
   2. ***NFT Mints*** - Detailing the specifics around mints of NFT projects

## **Governance/dREP Data**

With the Voltaire era in effect post-Chang hardfork, new data attributes onchain can be utilized to understand governance proposals interoduced as well as Intersect actions.  In addition, tracking voting and governance participation can be seen onchain

   1. ***dREP Participaton*** - A table filled with registered dREPs and their onchain participation actions within governance
   2. ***Governance Proposal*** - Metadata related to proposals that are successfully registered onchain as well as outcomes from subsequent votes

## **Stakepool Operators Data**

Cardano block producing and validation is managed through the stakepool setup in Cardano and the stakepool tables will be designed to higlight information specific to stakepools

   1. ***Active Stakepool Metrics*** - Operating onchain statistics around active stakepools.
   2. ***Staking Rewards and ISPO History*** - Highlighting rewards from staking distributed to users as well as metrics around pools that have participated in ISPOs.

**References**:

- [Cardano Fans Offchain Data Registry](https://github.com/Cardano-Fans/crfa-offchain-data-registry)
- [Cardano Foundation Token Registry](https://github.com/cardano-foundation/cardano-token-registry)
