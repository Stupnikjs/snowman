# SNOWMAN Vulnerabilities Report

## Overview

This report documents observed behaviors and logic flows related to the SNOWMAN protocol.
The focus is on high-level contract structure and exposed functionalities.

---

## SNOW Contract

### Description

- ERC20-based token logic
- Access to core functions restricted by `canFarmSnow` modifier

### Farming Conditions

- Farming availability depends on `block.timestamp`
- Actions are restricted if a predefined ending time is reached

### Purchase Logic

Users can acquire SNOW tokens using one of the following payment methods:
- Native ETH
- Wrapped token (`i_weth`)

```solidity
function buySnow(uint256 amount) external payable canFarmSnow

### Collector 

Collector can pass collector role to an other address seems like a secure behaviour


## SNOWMAN Contract 


- ERC721-based 


```bash
forge install foundry-rs/forge-std
``