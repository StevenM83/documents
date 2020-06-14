# Get BSC as a Bitcoin Holder

## How To Import BTC to BSC Wallet

If you hold bitcoin before the BitcoinSC hard fork, you can import those coins to BitcoinSC Core to claim BSC. There are two ways to accomplish this:

1. Import wallet and password from Bitcoin Core to BitcoinSC Core (copy wallet.dat file). This assumes you do not have existing BSC in the BitcoinSC wallet.
2. Import private keys from a Bitcoin wallet to BitcoinSC Core. This approach works with a new BitcoinSC wallet or one with existing BSC coins.

## Import Wallet

The wallet.dat file holds data for operating the wallet, including private keys. Use File – Import wallet, or you can simply move the wallet.dat file:

1. Exit Bitcoin Core. 
2. Find the “wallet.dat” file in the Bitcoin Core data directory -> wallets directory, and make a copy. 
3. Copy the “wallet.dat” file into the BitcoinSC Core data directory -> wallets directory as “wallet.dat”
4. Launch BitcoinSC Core. Make a backup of the wallet.

Bitcoin data directory locations https://en.bitcoin.it/wiki/Data_directory BitcoinSC follows the same pattern.

![Windows Def](https://user-images.githubusercontent.com/62684845/84581065-3812f200-adab-11ea-8dcd-26047c78058b.jpg  "Default location on Windows (testnet3)")
<p align="center">Default wallet.dat location on Windows (testnet3)</p>

## Import Private Key

Importing the private key gives more flexibility to import Bitcoin from a variety of wallets. 

On Bitcoin Core use the `dumpprivkey` command with for the address

![Bitcoin Dump Priv Key](https://user-images.githubusercontent.com/62684845/84581081-4a8d2b80-adab-11ea-98bb-782172c949d4.png "Bitcoin Core dumprivkey")

<p align="center">dumpprivkey mvu43DT2sKXqArYS4NEpDmnYUfq6C9vBTC result cMxDbqiaFAomy5kHwAgDwFfeza6Ru6gcu2EUQBfR6jiG8Quwyjfj</p>

On Electrum use Addresses then right-click on the desired address and choose “Private key”, enter the password and copy the private key.

![Electrum Priv Key](https://user-images.githubusercontent.com/62684845/84581087-55e05700-adab-11ea-9f13-c37c78ae1aaa.jpg "Electrum get Private Key")

To import on BitcoinSC Core use the `importprivkey` command. The wallet will Rescan.

![BitcoinSC Import Priv Key](https://user-images.githubusercontent.com/62684845/84581093-5d9ffb80-adab-11ea-92fd-e74dea306606.jpg "BSC Core importprivkey")

<p align="center">importprivkey mvu43DT2sKXqArYS4NEpDmnYUfq6C9vBTC cMxDbqiaFAomy5kHwAgDwFfeza6Ru6gcu2EUQBfR6jiG8Quwyjfj</p>

## About Addresses

The address format is identical between Bitcoin and BitcoinSC which means that addresses are not restricted for use between wallets. Please exercise caution because post-fork BSC can be sent to Bitcoin addresses and vice versa. If this happens with addresses where you have access to private keys, the coins can be recovered as shown above. If you transpose addresses sending coins to an exchange (exchanges TBD) only the exchange could recover the coins if they wanted to do that.

## Legacy, p2sh-SegWit, bech32

Legacy, p2sh-SegWit, and bech32 addresses and coins can be imported from Bitcoin to BitcoinSC using the techniques above. If a Bitcoin legacy private key is imported to BitcoinSC Core, then BitcoinSC Core will create 3 public addresses for legacy, p2sh-SegWit, and bech32. 

***

Live testnet3 addresses and private keys are shown.



