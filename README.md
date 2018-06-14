![EtherScamDB Logotype](https://github.com/MrLuit/EtherScamDB/blob/master/logo/logotype-readme.png?raw=true)

# Ethereum Scam Database

*An open-source database to keep track of all the current ethereum scams*

## Usage

Make sure you have both [Node.JS](https://nodejs.org/en/download/) and [Git](https://git-scm.com/downloads) installed.

Rename `config.exmaple.js` to `config.js` and replace the placeholders with your keys.

Then, open a command line anywhere and run the following commands:

> git clone https://github.com/MrLuit/EtherScamDB.git

> npm install

> node run.js

The command line should now exit, asking you to update the config.js file with correct values. Please use your own API keys. When you're done, launch run.js again:

> node run.js

Generating should take a couple of minutes the first time or after a clean, but when `cache.json` is already present it should launch instantly.

## Flags

- `--clean` Clean up all the old files and folders
- `--update` Manually update all content

## Contribute

Fork this project and edit `_data/data.yaml`. Every item can have the following properties:

- **id**: A unique incremental integer
- **name**: The title of the scam, should probably not be longer than 64 characters
- **status**: The status of a scam. If `status` isn't provided and `url` is, status will be autogenerated with the `--update` flag  **(Optional)**
- **description**: A full description for the scam **(Optional)**
- **url**: The protocol + hostname for a scam website, without a trailing `/` **(Optional)**
- **category**: The category under which the item falls **(Optional)**
- **addresses**: An array of all ethereum addresses that were involved in this scam, with leading '0x'  **(Optional)**

## API

To make use of our database, the following API can be used: https://etherscamdb.info/api/

## Donate

If you would like to help without contributing on GitHub yourself you can send some ETH or ERC20 tokens to [etherscamdb.eth](https://etherscan.io/address/etherscamdb.eth) :clap:

## Thanks

* Thanks to [Tobaloidee](https://github.com/Tobaloidee) for doing the logos!
