# TroFi Market

TroFi Market is a marketplace where merchants can sell rare *physical* assets - trophy assets.

Approved MERCHANTs can CREATE a new AUCTION. Anyone can be a BIDDER. SHAREHOLDERs own the system itself. SHAREHOLDERs must approve new MERCHANTS.

In order to be considered for approval, a MERCHANT should complete their profile information through the TroFi Market front end:
* Company name (SC)
* Their proposed listing fee, paid every time they list a new asset for sale (SC)
* Their proposed platform tax, calculated as a percentage of the final sale price (SC)
* A list of social media accounts and posts proving ownership of these accounts (IPFS)
* Examples of the types of items they propose to sell through the TroFi Market (IPFS)
* A government issued company registration certificate if they are a company, or a profile picture of themselves if they are an independent artist (IPFS) 
* A signed letter from the director of the company (if they are a company) requesting the shareholders to approve the application (IPFS)
* A contact email address, must be @ their company domain if it's a company

SHAREHOLDERS may then vote on approving the MERCHANT profile (>50% of shareholders must vote YES, and 0% must vote NO). If approved, the MERCHANT then has privileges to create new AUCTIONs.

### AUCTION creation:
* MERCHANT takes very detailed pictures (videos can also be used) of the item, along with any original documentation, box, receipts, etc (IPFS)
* MERCHANT uses the TroFi Market frontend to produce a Markdown document explaining the history and details of the item, including pictures etc from IPFS (IPFS)
* MERCHANT sets the toptime for the auction. This is how long a bid must remain the top bid in order to win the auction.
* MERCHANT must specify a Bitcoin, Ethereum, or contract native (BSC?) address for final settlement.
* MERCHANT launches the AUCTION, pushing it to the TroFi contract. The listing fee is deducted from their wallet.
* MERCHANT specifies a single global shipping + insurance price in USD, and a 1 year storage cost in USD in their listing.

### AUCTION process:
* BIDDERs can bid on the auction through the website by using Metamask.
* The bid price is denominated in Bitcoin.
* The BIDDER decides how much they want to bid, in BTC.
* The BIDDER must lock coins as a deposit in order to bid. The amount they need to lock is the platform tax for their bid amount. 
  * E.g. if the MERCHANT has a platform tax of 1%, and the user wants to bid 1 BTC, they need to lock 0.001BTC (or equivalent in other currencies). 
* The locked coins are unlocked and returned to the bidder if someone else outbids them.
* If the BIDDER remains the top bidder for the *toptime*, they have won the auction. The deposit is *not* returned to the bidder.
* When the AUCTION is completed (a BIDDER wins the auction), they have 24 hours to settle the final payment to the MERCHANT's address (BTC/ETH/BSC). Failure to do so means the merchant can restart the auction and the bidder loses their deposit. 
* The MERCHANT releases ownership of the PNFT to the winner upon recieving final settlement.
* The winning BIDDER then owns the PNFT. 

#### After the AUCTION has ended:
* The winner of the auction can request that the physical asset be shipped to them, or that it be stored by the merchant. 
* If the asset is shipped to the auction winner, the NFT status must be updated as no longer being in the custody of the merchant

#### Re-Auctioning of items
* The winner of the auction may only re-auction the item if the physical asset is in the custody of an approved MERCHANT. 
* The OWNER (winner of the auction) may ship the physical asset back to the MERCHANT if they wish to re-auction.


### Fixed Price Listings:
* MERCHANT’s can create a fixed price listing, denominated in BTC. The winner of a fixed price listing is simply the first one to buy it.
* MERCHANTS can delete their fixed price listings at any time.
* Global shipping and insurance cost must be built into the price by the merchant.

### Valid tokens for bidding and settlement
#### Bidding (BSC)
* BUSD-T
* BNB
* WBNB
* BUSD
* ETH
#### Settlement (BSC or native BTC)
* BTC
* BUSD-T
* BNB
* WBNB
* BUSD
* ETH

### TroFi Shares:
* SHAREHOLDERs are anyone who holds TroFi governance shares/tokens. 
* All profit (platform tax, and listing fee) of the TroFi Market is sent to SHAREHOLDERs, in proportion to the number of TroFi shares they own.
* 1,000,000 shares are initially created
* All future creation of shares must be approved by 90% of current shareholders

