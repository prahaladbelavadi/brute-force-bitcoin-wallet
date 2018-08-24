# brute-force-bitcoin-wallet
Brute forcing bitcoin wallet; silly attempt;

## Structure:

- Random 32bit number generated
- Public key pair from random number
- mnemonic created from random number
- Bitcoin address created
- Check from file to see if address matches.
  - If address matches:
   - return private key and mnemonic
 - if address does not match: 
 - try different random number
 
 ## Optimization:
 - eliminating same random numbers:
    random numbers are generated from cpu disk cycles in most cases which are prone to repetition, must check from file to see if the random number has already been tested for
  - parallel processing:
    single thread processing would take a significantly long time; parallel processing is important; wrapping it in docker is possible
  - sorting address file:
    address file must be sorted to input, check and verify new addresses; address file can check with mainnet to see if any existing address has funds
  - increasing key space:
    the address in addressfile can contain a list of all existing adddresses on the bitcoin blockchain, this increases the possibility of recovering an address with funds to spend 
  - try prdictive dictionary attack:
    most people use predictive source of randomness; using dictionary attacks at mnemonic and random number generation level 

 
