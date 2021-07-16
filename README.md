# Blockchain Instructions Homework

-Create a new project directory for your new network. Call it whatever you want!


-Create a "Screenshots" folder inside of the project directory


-Create accounts for two (or more) nodes for the network with a separate datadir for each using geth.
  -./geth --datadir node1 account new
  -./geth --datadir node2 account new

Please specify a network name to administer (no spaces, hyphens or capital letters please)
> networkname

What would you like to do? (default = stats)
 2. Configure new genesis

What would you like to do? (default = create)
 1. Create new genesis from scratch


Which consensus engine to use? (default = clique)
 2. Clique - proof-of-authority


How many seconds should blocks take? (default = 15)
> enter

Which accounts are allowed to seal? (mandatory at least one)
0x1111111111111111111111111111111111111111
0x2222222222222222222222222222222222222222


Which accounts should be pre-funded? (advisable at least one)
0x1111111111111111111111111111111111111111
0x2222222222222222222222222222222222222222


Should the precompile-addresses (0x1 .. 0xff) be pre-funded with 1 wei? (advisable yes)
> no

Specify your chain/network ID if you want an explicit one (default = random)
> 333 (use any 3 digit number -remeber to use the same number for your wallet)


What would you like to do? (default = stats)
 2. Manage existing genesis

 2. Export genesis configurations

What would you like to do? (default = stats)
 1. Show network stats
 2. Manage existing genesis
 3. Track new remote server
 4. Deploy network components
Use "control+c" to quit 



3 With the genesis block creation completed, we will now initialize the nodes with the genesis' json file.
Using geth, initialize each node with the new networkname.json

./geth --datadir node1 init networkname.json
./geth --datadir node2 init networkname.json


4 Now the nodes can be used to begin mining blocks.
Run the nodes in separate terminal windows with the commands:

./geth --datadir node1 --unlock "0x1111111111111111111111111111111111111111" --mine --rpc --allow-insecure-unlock

./geth --datadir node2 --unlock "0x2222222222222222222222222222222222222222" --mine --port 30304 --bootnodes "enode://0bf2163491e3ae70e1216667e2e1b84593189828c91f329fe9b650603ef33a11a0673d07e982395191b5d14c68e2ca99dd65432da9cd263bc714a85de77d3a0c@127.0.0.1:30303" --ipcdisable --allow-insecure-unlock

- Please specify a network name to administer (no spaces, hyphens or capital letters please)
  -networkname
   
  - What would you like to do? (default = stats)
    2. Configure new genesis

  - What would you like to do? (default = create)
    1. Create new genesis from scratch
    
-Choose the Clique (Proof of Authority) consensus algorithm.


-Paste both account addresses from the first step one at a time into the list of accounts to seal.


-Paste them again in the list of accounts to pre-fund. There are no block rewards in PoA, so you'll need to pre-fund.


-You can choose no for pre-funding the pre-compiled accounts (0x1 .. 0xff) with wei. This keeps the genesis cleaner.


-Complete the rest of the prompts, and when you are back at the main menu, choose the "Manage existing genesis" option.


-Export genesis configurations. This will fail to create two of the files, but you only need networkname.json.


-You can delete the networkname-harmony.json file.


-Screenshot the puppeth configuration once complete and save it to the Screenshots folder.

-Initialize each node with the new networkname.json with geth.


-Run the first node, unlock the account, enable mining, and the RPC flag. Only one node needs RPC enabled.


-Set a different peer port for the second node and use the first node's enode address as the bootnode flag.


-Be sure to unlock the account and enable mining on the second node!


-You should now see both nodes producing new blocks, congratulations!



-Send a test transaction


-Use the MyCrypto GUI wallet to connect to the node with the exposed RPC port.


-You will need to use a custom network, and include the chain ID, and use ETH as the currency.
