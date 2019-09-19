## COMMING SOON. Fully Decentralized, 99.99% "off block" if you choose, no need for gas to keep it crawling and secure and no smart contracts

### More info below Microsofts words. 
### NOTE: I'm passonate abou this stuff. Don't mistake that for pissyness. Conceptually, is the future of not only data processing, but the internet itself. And Microsoft is pretty much always on point.


# Decentralized & Collaborative AI on Blockchain

<img src="./assets/logo.gif?raw=true" width=500 alt="Animated logo for the project. A neural network appears on a block. The nodes change color until finally converging. The block slides away on a chain and the process restarts on the next blank block.">

<!-- Put horizontally since build status badges are normally horizontal. -->
| [Demo][demo-folder] | [Simulation][simulation-folder] | Security |
|:-:|:-:|:-:|
| [![Build Status](https://dev.azure.com/maluuba/0xDeCA10B/_apis/build/status/demo-CI?branchName=master)](https://dev.azure.com/maluuba/0xDeCA10B/_build/latest?definitionId=116&branchName=master) | [![Build Status](https://dev.azure.com/maluuba/0xDeCA10B/_apis/build/status/simulation-CI?branchName=master)](https://dev.azure.com/maluuba/0xDeCA10B/_build/latest?definitionId=117&branchName=master) | [![Build Status](https://dev.azure.com/maluuba/0xDeCA10B/_apis/build/status/Security%20Checks?branchName=master)](https://dev.azure.com/maluuba/0xDeCA10B/_build/latest?definitionId=118&branchName=master) |

**Decentralized & Collaborative AI on Blockchain** is a framework to host and train publicly available machine learning models.
Ideally, using a model to get a prediction is free.
Adding data consists of validation by three steps as described below.

<img src="./assets/architecture_flow.png?raw=true" width=500 alt="Picture of a someone sending data to the addData method in CollaborativeTrainer which sends data to the 3 main components as further described next.">

1. The **IncentiveMechanism** validates the request to add data, for instance, in some cases a "stake" or deposit is required. In some cases, the incentive mechanism can also be triggered later to provide users with payments or virtual "karma" points.
2. The **DataHandler** stores data and meta-data on the blockchain. This ensures that it is accessible for all future uses, not limited to this smart contract.
3. The machine learning **model** is updated according to predefined training algorithms. In addition to adding data, anyone can query the model for predictions **for free**.

The basics of the framework can be found in our [blog post][blog1].
A demo of one incentive mechanism can be found [here][demo].
More details can be found in the [initial paper][overview-paper] describing the framework, accepted to Blockchain-2019, The IEEE International Conference on Blockchain: (coming July 2019)

This repository contains:
* [Demos][demo-folder] showcasing some proof of concept systems using the Ethereum blockchain. There is a locally deployable test blockchain and demo dashboard to interact with smart contracts written in Solidity.
* [Simulation tools][simulation-folder] written in Python to quickly see how models and incentive mechanisms would work when deployed.

<img src="./assets/aka.ms 0xDeCA10B QR.png?raw=true" width=250 alt="Picture of a QR code with aka.ms/0xDeCA10B written in the middle.">

# FAQ/Concerns

## Aren't smart contracts just for simple code? 
There are many options.
We can restrict the framework to simple models: Perceptron, Naive Bayes, Nearest Centroid, etc.
We can also combine off-chain computation with on-chain computation in a few ways such as:
* encoding off-chain to a higher dimensional representation and just have the final layers of the model fine-tuned on-chain,
* using secure multiparty computation, or
* using external APIs, or as they are called the blockchain space, oracles, to train and run the model

We can also use algorithms that do not require all models parameters to be updated (e.g. Perceptron).
We hope to inspire more research in efficient ways to update more complex models.

Some of those proposals are not in the true spirit of this system which is to share models completely publicly but for some applications they may be suitable.
At least the data would be shared so others can still use it to train their own models.

## Will transaction fees be too high?
Fees in Ethereum are low enough for simple models: a few cents as of July 2019.
Simple machine learning models are good for many applications.
As described the previous answer, there are ways to keep transactions simple.
Fees are decreasing: Ethereum is switching to proof of stake.
Other blockchains may have lower or possibly no fees.

## What about storing models off-chain?
Storing the model parameters off-chain, e.g. using IPFS, is an option but many of the popular solutions do not have robust mirroring to ensure that the model will still be available if a node goes down.
One of the major goals of this project is to share models and improve their availability, the easiest way to do that now is to have the model stored and trained in a smart contract.

We're happy to make improvements! If you do know of a solution that would be cheaper and more robust than storing models on a blockchain like Ethereum then let us know by filing an issue!

## What if I just spam bad data?
This depends on the incentive mechanism (IM) chosen but essentially, you will lose a lot of money.
Others will notice the model is performing badly or does not work as expected and then stop contributing to it.
Depending on the IM, such as in Deposit, Refund, and Take: Self-Assessment, others that already submitted "good" data will gladly take your deposits without submitting any more data.

Furthermore, people can easily automatically correct your data using techniques from unsupervised learning such as clustering.
They can then use the data offline for their own private model or even deploy a new collection system using that model.

## What if no one gives bad data, then no one can profit?
That’s great!
This system will work as a source for quality data and models.
People will contribute data to help improve the machine learning models they use in their daily life.

Profit depends on the incentive mechanism (IM).
Yes, in in Deposit, Refund, and Take: Self-Assessment, the contributors will not profit and should be able to claim back their own deposits.
In the Prediction Market based mechanism, contributors can still get rewarded by the original provider of the bounty and test set.

# Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.microsoft.com.

When you submit a pull request, a CLA-bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., label, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

[demo-folder]: demo/
[simulation-folder]: simulation/

[demo]: https://aka.ms/0xDeCA10B-demo
[blog1]: https://aka.ms/0xDeCA10B-blog1
[overview-paper]: https://aka.ms/0xDeCA10B-paper

-----------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------
----------------------------------------------------------------------------------------------------

## My apologies Microsoft for not reaching out directly before I write this. 
But I'm a lttile hurt. I think Interperet is the best thing since sliced bread, 
CNTK is a no brainer and ONIX will hopfully save as much electrity Bitcoin and Etherium used. 

# While this is a brilliant project, engineers should not build NN's on a network where 
1. Could lose money sending bad data 
2. The heath of the network is tied to computation
3. it's fucking gas powered 
4. no parallelization 
5. A drop in price will screw the miners and open the network up to DDOS attacks. And via DAO's forck the chain forever. 
6. And this is the one that sould have anyone worries. concurrency. It cannot exist within the chain. 

If that sounds like the future of the internet, the finacial system and our appications, I woudn't even smoke whatever you're smoking. 

I will explain in deatil as I work on this code over the next few months. And I'll likly take this down. I hate complaining. But somtimes, you have to even if it's only for you. 

## Here is what you need

A small is a small, easy, and fast data sycronization protocol plus storage system that runs everywhere. While smart contract are easy to write, you need to focus on the data that needs to stored, loaded, and and seemlessly shared without worrying about servers, network calls, or tracking offline changes or concurrency conflicts. 

## How about this?

When a browser peer asks for data, it'll merge the reply with its own data using a CRDT, then cache the result. This means that:

1. The next time the browser asks for that data, the reply is instant, even when offline.
2. Data is replicated on each browser that asked for it.
3. If your server fails, you can still recover your data from the browsers.
4. This makes the loss of important information nearly impossible, as all copies of the data would need to be destroyed before it is lost.
5. No need to fart back and forth to keep hackers out and the network alive. 

## But that im impossible without being an AP system?

That's the point and a mute one. What you're lookling for is Strong not Eventual consistancy, right? Wrong. That system is not highly available. RThink abou it, if there is a network partition (I.e., if any one peer cannot be reached) the data cannot be said to be consistent without waiting an indefinite amount time. 

You don't need a locking system. The new new reserch is regrads to Convergent Replicated Data Types (CRDTs), Directed Acyclic Graphs (DAGs), Operational Transformation (a WOOT), and possibly Stellar. Look, if you're going to call somthing decentralised, don't centralise it. You define "dependent causality" explicitly in the data, rather than the protocol - and thus should be preferred since they (CRDT, DAG;s and WOOTs) give you some form of linearizability without sacrificing the advantages of a peer-to-peer system. Which is the whole fucking point. See you when this works. 

## FYI, this code it writen. Now I have to put my money wher my mouht is and replace etherium. 

SIDE NOTE: This exact concept was my next personal project. It's way over due. But since Microsoft is leaving everyone in the dust as far as AIML goes, I'm not suprised that this is already testable and when i replace the simple part, microsoft with have the 'set it and forget it'  offline first, fully distributed 

