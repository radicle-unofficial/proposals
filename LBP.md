# [Formal Review] Distribute LBP unsold tokens to the LBP holders in proportion to their contribution

> WIP

```
>- {Snapshot Poll} -<
```

## Functional Description

It's being proposed that distrubuting 151614.2475 RAD from Radicle Treasury with 6
months' lock time to [the LBP holders][hd] who holds 559728.7298901365 RAD from the
LBP till now.

1. Count the LBP holders, maybe base on [this script][ts]
2. Distribute RAD to the holders


## Purpose

This distribution would help the project by putting more votes into the hands of individual
community members for helping radicle being more decentralized. 

As the first proposal not drafted by the core team, this proposal could be a template for 
more community driven proposals, and it would encourage more community members joining the
governance of radicle.

The amount of this distrubution depends on the UNIX timestamp of the first commit of [OSCOIN][oc], 
the date, the dream starts, for regarding and respecting the perseverance of the Radicle Team.



## Background

On February 25th, ~3.75% of the Radicle token supply available for interested parties within the 
Radicle community. It used Balancer a decentralized exchange and leverages a mechanism called 
Liquidity Bootstrapping.

Over 1800 new token holders participated in the event, claiming over 50% of the RAD tokens put 
on Balancer at the beginning of the event. This event raised ~$25M in the Radicle Treasury, a 
smart contract controlled fully and transparently by Radicle token holders.

Since [Exit LBP & add Uniswap liquidity?][ea], the unsold RADs has been back to the radicle 
treasury, and after [transfering 287k RADs to uniswap pool][tl], there are around 1.45M RADs
left from LBP.

Early supporters of Radicle were able to become part of the community by buying the Rad token for 
$1.5 USD. LBP supporters paid between $10 and $30. LBP contributors support the project just as much 
As the early backers who were allowed to join in for just $1.5 and should be rewarded for it with a 
share of the unsold tokens. There are already more than enough tokens available in the treasury to 
be used for other purposes.



## Link to previous discussions

* https://radicle.community/t/discussion-should-unsold-rad-be-distributed-amongst-lbp-contributors/1527

* https://radicle.community/t/discussion-should-the-remaining-rad-balances-from-the-lbp-event-be-distributed-amongst-lbp-contributors/1674

* https://radicle.community/t/structured-discussion-distribute-lbp-unsold-tokens-to-the-people-who-contributed-to-the-lbp-in-proportion-to-their-contribution/1944



## Reasoning & analysis

The community has been disicussed this proposal for really a long time, except the purpose
metioned above, we took several polls for surveying should we put forward this proposal.

* https://radicle.community/t/structured-discussion-distribute-lbp-unsold-tokens-to-the-people-who-contributed-to-the-lbp-in-proportion-to-their-contribution/1944/42

  * Distribute 50% unsold tokens to the LBP contributors
  * Only distribute tokens to the LBP contributors who haven't sold their token
  * Distrubute RADs by how many RADs he/she exchanged in LBP
  * Set a limit for distributing RADs to one contributor

* https://radicle.community/t/structured-discussion-distribute-lbp-unsold-tokens-to-the-people-who-contributed-to-the-lbp-in-proportion-to-their-contribution/1944/58

  * Lock the distributing RADs for 6 months
  * Unlock the distrubuting RADs every 6 weeks
  * Unlock fixed proportion everytime unlock

* https://radicle.community/t/structured-discussion-distribute-lbp-unsold-tokens-to-the-people-who-contributed-to-the-lbp-in-proportion-to-their-contribution/1944/69

  * Continue this proposal

* https://radicle.community/t/structured-discussion-distribute-lbp-unsold-tokens-to-the-people-who-contributed-to-the-lbp-in-proportion-to-their-contribution/1944/73

  * Distribute tokens by the UNIX epoch timestamp of the initial commits of OSCOIN, the date, the dream starts.


In the last poll we vote distributing 15161.42475 RAD, 0.027 per RAD, after calcuating it over again,
it can not achieve the purpose putting more votes into the hands of individual community members, so
it is 151614.2475 RAD now.



## Technical Implementation

Transfering the distributed RAD to LBP holders one by one takes too much gas, this proposal
requires a function in [radicle-contracts][rc] that can drop or set claimable RAD to the LBP
holders' address.



## Impact

The LBP holders are not selling their RAD in a short time, instead they hold their RAD for 
the longest time, this proposal hardly can add liquidity to the market but distribute more 
votes to the individual community members, besides, this will encourage more community members 
holding their RAD.



## Open Questions

* There is a lot of community members join radicle as holders after the LBP, how could we set a 
mechanism benefiting the RAD holders?

* It seems [radicle-contracts][rc] doesn't have a function that can execute this proposal 
immediately, if it passes, who will be writing the code?


[sd]: https://radicle.community/t/structured-discussion-distribute-lbp-unsold-tokens-to-the-people-who-contributed-to-the-lbp-in-proportion-to-their-contribution/1944/79
[oc]: http://oscoin.io/
[ea]: https://snapshot.org/#/gov.radicle.eth/proposal/QmVypVPUPzHkM4VWSdVx5DHL7o2Xxxvydd85dEQaEyh9Fg
[tl]: https://etherscan.io/token/0x31c8eacbffdd875c74b94b077895bd78cf1e64a3?a=0x8da8f82d2bbdd896822de723f55d6edf416130ba
[hd]: https://github.com/radicle-unofficial/holders/blob/main/lbp_holders.json
[rc]: https://github.com/radicle-dev/radicle-contracts
[ts]: https://github.com/radicle-unofficial/holders
