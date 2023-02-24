# Chain-Upgrade-on-Cosmos-Node

Once the chain reaches the upgrade height, you will encounter the following panic error message:

`ERR UPGRADE "xxx" NEEDED at height: 7545xx`

Here is the command (I use Stride Node for example)
```
sudo systemctl stop <strided>
cd $HOME && rm -rf <stride>
git clone <https://github.com/Stride-Labs/stride.git> && cd <stride>
git checkout <v2.0.3>
make build
sudo mv build/<strided> $(which <strided>)
sudo systemctl restart <strided> && journalctl -fu <strided> -o cat
```
