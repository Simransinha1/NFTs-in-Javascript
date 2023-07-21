Assessment Requirements
1. Create a variable that can hold a number of NFT's. What type of variable might this be?
2. Create an object inside your mintNFT function that will hold the metadata for your NFTs. 
   The metadata values will be passed to the function as parameters. When the NFT is ready, 
   you will store it in the variable you created in step 1
3. Your listNFTs() function will print all of your NFTs metadata to the console (i.e. console.log("Name: " + someNFT.name))
4. For good measure, getTotalSupply() should return the number of NFT's you have created



const nftsCollection = [];
function mintNFT(name, hairColor, shirtType, accessory) {
  
  const nft = {
    name: name,
    hairColor: hairColor,
    shirtType: shirtType,
    accessory: accessory,
  };

  
  nftsCollection.push(nft);
}
function listNFTs() {
  
  nftsCollection.forEach((nft, index) => {
    console.log(`NFT ${index + 1}:`);
    console.log("Name: " + nft.name);
    console.log("hair Color: " + nft.hairColor);
    console.log("Shirt Type: " + nft.shirtType);
    console.log("accessory: " + nft.accessory);
    console.log("------------------");
  });
}
function getTotalSupply() {
  return nftsCollection.length;
}

mintNFT("NFT 1", "Gray", "Polo Shirt", "Sunglasses");
mintNFT("NFT 2", "Purple", "Tank Top", "Necklace");
mintNFT("NFT 3", "Black", "Long Sleeve", "Platinum Watch");


listNFTs();
console.log("Total NFTs: " + getTotalSupply());
