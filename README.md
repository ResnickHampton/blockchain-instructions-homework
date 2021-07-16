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

./geth --datadir node2 --port 30304 --rpc --bootnodes "enode://<replace with node1 enode address>"





-Send a test transaction


-Use the MyCrypto GUI wallet to connect to the node with the exposed RPC port.


-You will need to use a custom network, and include the chain ID, and use ETH as the currency.
