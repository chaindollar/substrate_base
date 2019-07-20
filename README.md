# Installation



```
git clone https://github.com/chaindollar/substrate_base

cd substrate-base/

//安装substrate
curl https://getsubstrate.io -sSf | bash -s -- --fast


//build 项目《substracte-node-template》
cd substrate-node-template
./scripts/init.sh
./scripts/build.sh
cargo build --release

//run 公有链接点
./target/release/node-template purge-chain --dev

./target/release/node-template --dev

//Substrate-admin

https://polkadot.js.org/apps/




substrate-node-new substrate-node-template <author-name>
substrate-ui-new substrate
```





# substrate-ui



```
substrate-ui-new substrate

Cd substrate-ui

yarn run dev


```

Substrate-ui 

<http://localhost:8000/>











# 卸载



```
./target/release/node-template purge-chain --dev

cd ~

rm -rf substrate-package
```


test001
