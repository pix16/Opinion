A Voting Station Smart Contract that allows making propositions and voting on them.
 - Proposals support several options: Yes/No, 5 stars, custom choices.
 - Voter can get a virtual sticker as an NFT.
 - Another NFT can be used a a virtual voter card.

The following current limitations still need to be addressed:
- String input validation
- Better SVG visuals for the NFT.
- Option to withdraw funds should any be sent to the contract.

Contract currently deployed on Rinkeby with address [0x42e6f47cfd09485a16d155349a77f3340b3b3c0e](https://rinkeby.etherscan.io/address/0x42e6f47cfd09485a16d155349a77f3340b3b3c0e)
Sample 'I Voted' sticker NFT on [opensea.io](https://testnets.opensea.io/assets/0x42e6f47cfd09485a16d155349a77f3340b3b3c0e/0).

API Overview:
```
function NewProposition( //Other flavors of the method available
        string memory description, // What is the Proposition about?
        OptionsType optionsType, // 0: No/Yes, 1: FiveStars, 2: SingleOption
        uint startDelayInHours, // delay from current time for voting to open
        uint voteDurationInHours // duration of voting window once it starts
    )
   
function VoteGetStickerAsNft( //Other flavors on the method available
        uint proposition, //Proposition Id
        uint choice // EXample, if proposal has option type 0 (No/Yes), choice can be 0 (No) or 1 (Yes)
    ) public returns (uint _voteNftId)
 ```
 
        
