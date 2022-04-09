# MATRIX-MINER

Enterprise of minig create your own coin 
https://github.com/P7-33/BROWS-COIN.wiki.git
[(ambas licencias BSD)]

Code
Issues
246
Pull requests
9
Actions
Projects
Wiki
Security
Insights
 3.0.5.0 
https://choosealicense.com/licenses/mit/

luc1an24 Update Plugins.md
…
 1 contributor:
https://composer.github.io/installer.sha384sum

RawBlame
 
Plugins
What is a Plugin?
What is MinerPluginToolkitV1 used for?
List of included plugins
What is a Plugin?
A plugin is an external or internal dependcy (dll). The ABI (Application Binary Interface) is defined in MinerPlugin project and plugin developers must implement the following interfaces IMinerPlugin and IMiner. This means that you create a new project inside Miners directory and implement all required functions from IMinerPlugin and IMiner interfaces. It is recommended that each one is in its own file (Plugin and Miner file).

Each plugin project should implement at least 1 plugin. You can implement more, but good practice is to keep 1 plugin inside 1 project.
IMinerPlugin is used for registering the plugin and there will be only 1 instance created. Its job is to give basic info such as name, UUID, version, etc.
IMiner is the mandatory interface for all miners containing bare minimum functionalities and is being used as miner process instance created by IMinerPlugin.

Bare minimum example of plugin is written in Example Plugin project. The Plugin file contains implementation of IMinerPlugin interface for registration and creation of the plugin instance. The Miner file contains implementation of IMiner interface, providing required functionalities.

What is MinerPluginToolkitV1 used for?
It is recommended to use MinerPluginToolkitV1 as this will enable full integration with Browser mining. It will save time developing it and enable implementation of additional advanced features. If you are writing a plugin we highly recommend that you use MinerPluginToolkitV1. All miner plugins that are developed by Browser miner dev team are using MinerPluginToolkitV1. For example you can check GMiner Plugin.

MinerPluginToolkitV1 also enables creation of Background Services, check out Ethlargement plugin for example.

Advantages	Disadvantages
Implementation of all basic actions like Start/Stop mining, Start benchmarking, retrieve data from API, create command line, etc.

Use of additional features like Configs and Extra Launch Parameters

Access to usefull interfaces providing features like checking for missing files, device cross referencing, initializing internal settings, etc.

The current API is not final and might change in the future.

List of Included Plugins
Miner Plugins
All devices
Xmr-Stak
NVIDIA and AMD
BMiner
ClaymoreDual
GMiner
Phoenix
LolMiner
NanoMiner
NVIDIA
CCMiner
NBMiner
T-Rex
TT-Miner
CryptoDredge
MiniZ
Z-Enemy
AMD
SGMiner
TeamRedMiner
WildRig
CPU
XMRig
Background Services
Ethlargement Pill
© 2020 GitHub, Inc.
Terms
Privacy
Security
Status
Help
Contact GitHub
Pricing
API
Training
Blog
ambas licencias BSD

**Example output:**

`https://api..com/stats`:

```json
{
  "data": {
    "bitcoin": {
      "data": {
        "blocks": 599952,
        ...
      }
    },
    "bitcoin-cash": {
      "data": {
        "blocks": 605134,
        ...
      }
    },
    "bitcoin-sv": {
      "data": {
        "blocks": 604886,
        ...
      }
    },
    "ethereum": {
      "data": {
        "blocks": 8766052,
        ...
      }
    },
    "litecoin": {
      "data": {
        "blocks": 1721519,
        ...
      }
    },
    "dogecoin": {
      "data": {
        "blocks": 2941267,
        ...
      }
    },
    "dash": {
      "data": {
        "blocks": 1156197,
        ...
      }
    },
    "ripple": {
      "data": {
        "ledgers": 50795982,
        ...
      }
    },
    "groestlcoin": {
      "data": {
        "blocks": 2801282,
        ...
      }
    },
    "stellar": {
      "data": {
        "ledgers": 26968006,
        ...
      }
    },
    "monero": {
      "data": {
        "blocks": 2014108,
        ...
      }
    },
    "cardano": {
      "data": {
        "blocks": 3673733,
        ...
      }
    },
    "zcash": {
      "data": {
        "blocks": 756512,
        ...
      }
    },
    "mixin": {
      "data": {
        "snapshots": 18632532,
        ...
      }
    },
    "tezos": {
      "data": {
        "blocks": 974144,
        ...
      }
    }
  },
  "context": {
    "code": 200,
    ...
    }
  }
}
```

**Request cost 
**Example output:**

`https://api..com/bitcoin/stats`:

```json
{
  "data": {
    "blocks": 586962,
    "transactions": 438436033,
    "outputs": 1175789668,
    "circulation": 1783699604497237,
    "blocks_24h": 133,
    "transactions_24h": 302792,
    "difficulty": 9013786945891.7,
    "volume_24h": 203868415027354,
    "mempool_transactions": 11206,
    "mempool_size": 9700111,
    "mempool_tps": 3.183333333333333,
    "mempool_total_fee_usd": 17385.9233,
    "best_block_height": 586961,
    "best_block_hash": "0000000000000000000c0f21dffb88b43aaa38dc561c1744f8964c010ddeed5e",
    "best_block_time": "2019-07-25 13:40:20",
    "blockchain_size": 231910648585,
    "average_transaction_fee_24h": 18150,
    "inflation_24h": 166250000000,
    "median_transaction_fee_24h": 9812,
    "cdd_24h": 53734025.51903,
    "largest_transaction_24h": {
      "hash": "89037b97c0e8b7762c05c64ff89349e55433c7f2aaa5829dcf401774ad36d171",
      "value_usd": 323700000
    },
    "nodes": 9287,
    "hashrate_24h": "59651648914812891495",
    "inflation_usd_24h": 16578450,
    "average_transaction_fee_usd_24h": 1.8099929306260403,
    "median_transaction_fee_usd_24h": 0.97845264,
    "market_price_usd": 9972,
    "market_price_btc": 1,
    "market_price_usd_change_24h_percentage": 2.77893,
    "market_cap_usd": 177983139916,
    "market_dominance_percentage": 64.48,
    "next_retarget_time_estimate": "2019-08-06 08:06:58",
    "next_difficulty_estimate": 9154306812972,
    "countdowns": [
      {
        "event": "Reward halving",
        "time_left": 25822200
      }
    ],
    "suggested_transaction_fee_per_byte_sat": 49
  },
  "context": {
    "code": 200,
    ...
  }
}
```

`https://api..com/monero/raw/outputs?txhash=8e6a144dee7537a38e87f30e7c1f2bc1a35e5ef8b5032dfa7cf89a2df3073c41&address=44AFFq5kSiGBoZ4NMDwYtN18obc8AemS33DBLWs3H7otXft3XjrpDtQGv7SqSsaBYBb98uNbr2VBBEt7f2wfn3RVGQBEP3A&viewkey=f359631075708155cc3d92a32b75a7d02a5dcf27756707b47a2b31b21c389501&txprove=1`:

```json
{
  "data": {
    "address": "42f18fc61586554095b0799b5c4b6f00cdeb26a93b20540d366932c6001617b75db35109fbba7d5f275fef4b9c49e0cc1c84b219ec6ff652fda54f89f7f63c88",
    "outputs": [
      {
        "amount": 800000000000,
        "match": false,
        "output_idx": 0,
        "output_pubkey": "2b0d6d7573895be2fccb06bf83099a4dddf3f73656f18e2b96eab997571a640d"
      },
      {
        "amount": 1000000000000,
        "match": false,
        "output_idx": 1,
        "output_pubkey": "543c158062f43c11ac16ff90dea61728a41410ffeccea4cea65a6ba6fb83ccab"
      },
      {
        "amount": 10000000000000,
        "match": false,
        "output_idx": 2,
        "output_pubkey": "122b7ba237e82ca95d620f286761b8f8102fa346df8d982c6fe48003d3939c60"
      },
      {
        "amount": 10000000000000,
        "match": false,
        "output_idx": 3,
        "output_pubkey": "7ba5f4dc9acf62c6bca171ac8e81f7757050a480bbe20f2d1836086aa23f004f"
      },
      {
        "amount": 300000000000000,
        "match": false,
        "output_idx": 4,
        "output_pubkey": "597a3bd3e7a7007fb2bb11cd734731e388ee95f436f6aa07d0d7afe927b7faad"
      }
    ],
    "tx_hash": "8e6a144dee7537a38e87f30e7c1f2bc1a35e5ef8b5032dfa7cf89a2df3073c41",
    "tx_prove": true,
    "viewkey": "f359631075708155cc3d92a32b75a7d02a5dcf27756707b47a2b31b21c389501"
  },
  "context": {
    "code": 200,
    "results": 1,
    "state": 2014050,
    ...
  }
}
