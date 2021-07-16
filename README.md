# blockchain-instructions-homework
# Blockchain Homework 18Setup the custom out-of-the-box blockchain

<ul>
  <li>Create a new project directory for your new network. Call it whatever you want!</li>


<li>Create a "Screenshots" folder inside of the project directory.</li>


<li>Create accounts for two (or more) nodes for the network with a separate datadir for each using geth.</li>


<li>Run puppeth, name your network, and select the option to configure a new genesis block.</li>


<li>Choose the Clique (Proof of Authority) consensus algorithm.</li>


<li>Paste both account addresses from the first step one at a time into the list of accounts to seal.</li>


<li>Paste them again in the list of accounts to pre-fund. There are no block rewards in PoA, so you'll need to pre-fund.</li>


<li>You can choose no for pre-funding the pre-compiled accounts (0x1 .. 0xff) with wei. This keeps the genesis cleaner.</li>


<li>Complete the rest of the prompts, and when you are back at the main menu, choose the "Manage existing genesis" option.</li>


<li>Export genesis configurations. This will fail to create two of the files, but you only need networkname.json.</li>


<li>You can delete the networkname-harmony.json file.</li>


<li>Screenshot the puppeth configuration once complete and save it to the Screenshots folder.

<li>Initialize each node with the new networkname.json with geth.


<li>Run the first node, unlock the account, enable mining, and the RPC flag. Only one node needs RPC enabled.


<li>Set a different peer port for the second node and use the first node's enode address as the bootnode flag.


<li>Be sure to unlock the account and enable mining on the second node!


<li>You should now see both nodes producing new blocks, congratulations!



<li>Send a test transaction


<li>Use the MyCrypto GUI wallet to connect to the node with the exposed RPC port.


<li>You will need to use a custom network, and include the chain ID, and use ETH as the currency.
