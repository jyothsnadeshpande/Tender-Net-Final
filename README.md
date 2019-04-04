# TENDER-NET

This blockchain project has been built on Hyperledger Composer.Its functionalities include the following.

1.Conducting Reverse Auction of Government Tenders  and once the auction gets over, monitoring the contract until the contract gets over and consulting the stakeholders of the project for checking the genuinity of each transaction of the contract.
  It has been implemented in the following parts.

Bidding:

This business network defines:

Participants: 
  Member 
  Auctioneer

Assets: 
  Tender 
  TenderListing

Transactions: Offer CloseBidding

The makeOffer function is called when an Offer transaction is submitted. The logic simply checks that the listing for the offer is still for sale, and then adds the offer to the listing, and then updates the offers in the VehicleListing asset registry.

The closeBidding function is called when a CloseBidding transaction is submitted for processing. The logic checks that the listing is still for sale, sorts the offers by bid price, and then if the reserve has been met, transfers the ownership of the vehicle associated with the listing to the highest bidder. Money is transferred from the buyer's account to the seller's account, and then all the modified assets are updated in their respective registries.

To test this Business Network Definition in the Test tab:
