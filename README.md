# Solidity_Payment
State Variables:

baseURI: Base URI for metadata of NFTs.
baseExtension: Extension to append to the token URI.
cost: Cost in Ether to mint one NFT.
maxSupply: Maximum total supply of NFTs.
maxMintAmount: Maximum number of NFTs that can be minted in a single transaction.
paused: Flag indicating whether minting is paused.
whitelisted: Mapping of addresses that are whitelisted (allowed to mint without cost restrictions).
payments: Address to which payments are sent.
Constructor:

Initializes the contract with the provided parameters, sets the base URI, and mints 20 NFTs to the contract deployer.
Internal Function _baseURI():

Overrides the internal function to return the base URI.
Public Function mint():

Allows users to mint NFTs by providing the recipient's address and the number of NFTs to mint.
Checks for various conditions, including whether minting is paused, the mint amount is within limits, and the sender has provided enough Ether (unless whitelisted).
Public Function walletOfOwner():

Returns an array of token IDs owned by a given address.
Override Function tokenURI():

Overrides the ERC721 tokenURI function to provide the URI for a given token ID.
Owner-Only Functions:

setCost, setmaxMintAmount, setBaseURI, setBaseExtension: Allow the owner to update various contract parameters.
pause: Allows the owner to pause or unpause minting.
Whitelisting Functions:

whitelistUser, removeWhitelistUser: Allow the owner to add or remove addresses from the whitelist.
Owner-Only Function withdraw():

Allows the owner to withdraw funds from the contract.
This contract essentially represents an ERC-721 NFT contract with additional features such as a cost for minting, whitelisting, and the ability for the owner to manage various parameters. The contract also handles the minting process and metadata generation for the NFTs.





