// Create a variable to hold your NFTs
let nfts = [];

// This function will take in some values as parameters, create an
// NFT object using the parameters passed to it for its metadata, 
// and store it in the variable above.
function mintNFT(name, eyeColor, shirtType, bling) {
    const nft = {
        name: name,
        eyeColor: eyeColor,
        shirtType: shirtType,
        bling: bling
    };
    nfts.push(nft);
}

// Create a "loop" that will go through an "array" of NFT's
// and print their metadata with console.log()
function listNFTs() {
    nfts.forEach((nft, index) => {
        console.log(`NFT ${index + 1}:`);
        console.log(`  Name: ${nft.name}`);
        console.log(`  Eye Color: ${nft.eyeColor}`);
        console.log(`  Shirt Type: ${nft.shirtType}`);
        console.log(`  Bling: ${nft.bling}`);
        console.log('----------------------');
    });
}

// Print the total number of NFTs we have minted to the console
function getTotalSupply() {
    return nfts.length;
}

// Call your functions below this line
mintNFT("CryptoPanda", "Blue", "Hoodie", "Gold Chain");
mintNFT("DigitalDragon", "Green", "T-Shirt", "Silver Ring");
mintNFT("VirtualUnicorn", "Pink", "Dress", "Diamond Tiara");

listNFTs();
console.log(`Total Supply: ${getTotalSupply()}`);
