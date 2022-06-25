## Purpose is to take a fresh Ubuntu installation and deploy everything necessary to have Sifnoded 0.13.3 deployed and ready for confirgation.

<br>

### To be installed:
- GIT<br>
- GCC<br>
- Make<br>
- jq<br>
- GO v1.18.3<br>
- Sifnode v0.13.3<br>
- Cosmovisor v1.0.0<br>


<br>

### Process: <br>
   - Update and Upgrade OS. <br>
- Check for GIT, GCC, Make and jq.<br>
    - Install missing, if any. <br>
- Check for previous version of GO<<br>
    - remove older version from $HOME and/or /usr/local/bin/<<br>
- Download and Install go 1.18.3.linux-amd64 in $HOME<<br>
    - the version can be modified at the top of /src/main.sh<<br>
- Sys link $HOME/go/bin/go /usr/local/bin/go<br>
- Deploying Sifnoded v0.13.3.<br>
- Deploying Cosmovisor 1.0.0<br>
- Export necessery system variables to var.var<br>
- Sys link $HOME/.sifnoded/cosmovisor/genesis/bin/sifnoded /usr/local/bin/sifnoded<br>
- Final test of sifnoded version<br>
  
### At this point, everything is on place and Sinode is ready for setup. 
 
<br>
Note: Self-thought. This is my first full script and I welcome any constructive feedback. @dSebster or dsebster@vnodes.cloud


<br>

## INSTRUCTIONS:
- Download GIT from your home folder and run the install.sh script:<br>
   - ````git clone https://github.com/dSebster/vNodes.git && bash vNodes/install.sh```` <br>
- Move to the vNodes folder<br>
   - ```cd vNodes```<br>
- Run the install and deployment script<br>
   - ```bash install.sh```<br>
- Enter password for sudo<br>
- You will need to check and approve services restart along the way. <br>
   - hit OK and restart whatever services are already checked off.<br>

- Once the installation is finish, ource the variables:<br>
   - ````source var.var````<br>
  
  that's it. Now you can configure your node. 
  
  https://github.com/Sifchain/sifchain-validators/blob/master/docs/nodes/setup/standalone/manual.md
  
  About mid page, pick up at " For BetaNet: sifnoded init my-node --chain-id sifchain-1 "
    
