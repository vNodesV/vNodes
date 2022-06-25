## Purpose is to take a fresh Ubuntu installation and deploy everything necessary to have Sifnoded 0.13.3 deployed and ready for confirgation.



### To be installed:
- GIT
- GCC
- Make
- jq
- GO v1.18.3
- Sifnode v0.13.3
- Cosmovisor v1.0.0




### Process: 
   - Update and Upgrade OS. 
- Check for GIT, GCC, Make and jq.
    - Install missing, if any. 
- Check for previous version of GO<
    - remove older version from $HOME and/or /usr/local/bin/<
- Download and Install go 1.18.3.linux-amd64 in $HOME<
    - the version can be modified at the top of /src/main.sh<
- Sys link $HOME/go/bin/go /usr/local/bin/go
- Deploying Sifnoded v0.13.3.
- Deploying Cosmovisor 1.0.0
- Export necessery system variables to var.var
- Sys link $HOME/.sifnoded/cosmovisor/genesis/bin/sifnoded /usr/local/bin/sifnoded
- Final test of sifnoded version
  
### At this point, everything is on place and Sinode is ready for setup. 
 

Note: Self-thought. This is my first full script and I welcome any constructive feedback. @dSebster or dsebster@vnodes.cloud




## INSTRUCTIONS:
- Download GIT from your home folder and run the install.sh script:
   ```
   git clone https://github.com/dSebster/vNodes.git && bash vNodes/install.sh
   ``` 
- Enter password for sudo
- You will need to check and approve services restart along the way. 
   - hit OK and restart whatever services are already checked off.

- Once the installation is finish, ource the variables:
   ```
   source var.var
   ```
  
  
  that's it. Now you can configure your node. 
  
  https://github.com/Sifchain/sifchain-validators/blob/master/docs/nodes/setup/standalone/manual.md
  
  About mid page, pick up at " For BetaNet: sifnoded init my-node --chain-id sifchain-1 "
    
