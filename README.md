// create a variable to hold your NFT's
let nfts = [];

// this function will take in some values as parameters, create an
// NFT object using the parameters passed to it for its metadata, 
// and store it in the variable above.
function mintNFT(name, description, imageUrl) {
  let nft = {
    name: name,
    description: description,
    image: imageUrl
  };
  nfts.push(nft);
}

// create a "loop" that will go through an "array" of NFT's
// and print their metadata with console.log()
function listNFTs() {
  for (let i = 0; i < nfts.length; i++) {
    let nft = nfts[i];
    console.log("Name: " + nft.name);
    console.log("Description: " + nft.description);
    console.log("Image URL: " + nft.image);
    console.log("---");
  }
}

// print the total number of NFTs we have minted to the console
function getTotalSupply() {
  return nfts.length;
}

// call your functions below this line
mintNFT("UZAIR", "This is the first NFT", "https://example.com/nft1.jpg");
mintNFT("UMAIR", "This is the second NFT", "https://example.com/nft2.jpg");
mintNFT("UMER", "This is the third NFT", "https://example.com/nft3.jpg");

listNFTs();

let totalSupply = getTotalSupply();
console.log("Total Supply: " + totalSupply);
