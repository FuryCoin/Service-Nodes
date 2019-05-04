# Service-Nodes

# On Windows:

## Step 1: Downloads
Download windows cli wallet: [wallet](https://github.com/FuryCoin/Fury/releases/download/2.0.0/Fury_2.0.0_win-cli.zip)
Download blockchain [Blockchain](https://drive.google.com/open?id=1VtD9shKDlKV5wYYUUe23eSKQHa-DVkSa)
Download batch file that will open your wallet and daemon[Bat](https://drive.google.com/open?id=1Ib4DPVNbXvjRMORTO74Bw4wH5679OsMC)

## Step 2: Moving Files
Unzip cli wallet and move folder to where you would like to keep it.
Unzip batch file and put it in the same folder as the cli wallet.
Open the batch file to start your wallet and daemon (daemon needs to be started with --service-node . Batch file does this for you.).
Close the wallet and daemon after it has started to sync.
Open folder "C:\ProgramData\Fury\lmdb" and replace the data.mdb file with the one you downloaded.
If you cant navigate to that folder you need to change your settings to show hidden folders.
Open the batch file to start your wallet and daemon.

## Step 3: Setup
After daemon says it is done syncing make a wallet or open one you already have.
If you make a wallet be sure to backup your seed words.
Copy your wallet address.
In the daemon type prepare_registration and hit enter.
Type Y if you will be staking it yourself and hit enter.
Paste in your fury address and hit enter.
Type Y and hit enter to confirm the information you entered is correct.
Copy the registration that is output in the daemon.
Paste the output into your wallet and hit enter.
Type in your password and hit enter.
Type Y and hit enter to confirm the fee.
If you get an error you most likely have too many transactions in your wallet and you will need to sweep your wallet.
Congratulations you now are running a service node.  You do not need to keep the wallet open but you do need to have the daemon open at all times.  There is a 12 hour confirmation window so if your node goes down you have some time to get it back up.  If your node is down for too long though it will get kicked off of the SN network and you will need to wait 15 days before you get your stake back.

## Step 4: De-register
Open your CLI wallet and type request_stake_unlock (service node pubkey) and hit enter.
You can get your service node pubkey from the service node daemon you are running.  It is shown when you start the daemon.
Confirm.
Your stake will be active for another 15 days before it is cancelled.
