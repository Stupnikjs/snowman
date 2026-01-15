# ERROR MANAGING SNOWMAN MINTING PERMISSION 

Anyone can call this func directly from snowman contract and get free Snowmans

'''solidity 
function mintSnowman(address receiver, uint256 amount) external {
    for (uint256 i = 0; i < amount; i++) {
        _safeMint(receiver, s_TokenCounter);
        emit SnowmanMinted(receiver, s_TokenCounter);
        s_TokenCounter++;
    }
}
'''


## Correction 

this '''mintSnowman''' func should be accessible only from airdrop contract 