# Installation



```
git clone https://github.com/chaindollar/substrate_base

cd substrate_base/

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

新的substrate-ui中需要修改一下文件 ./src/app.jsx

主要是在底部增加一下代码
```
class DemoSegment extends React.Component {
	constructor() {
	  super()
	  this.player = new Bond
	}
  
	render() {
	  return <Segment style={{ margin: '1em' }} padded>
		<Header as='h2'>
		  <Icon name='game' />
		  <Header.Content>
			Play the game
			<Header.Subheader>Play the game here!</Header.Subheader>
		  </Header.Content>
		</Header>
		<div style={{ paddingBottom: '1em' }}>
		  <div style={{ fontSize: 'small' }}>player</div>
		  <SignerBond bond={this.player} />
		  <If condition={this.player.ready()} then={<span>
			<Label>Balance
			  <Label.Detail>
				<Pretty value={runtime.balances.balance(this.player)} />
			  </Label.Detail>
			</Label>
		  </span>} />
		</div>
		<TransactButton
		  content="Play"
		  icon='game'
		  tx={{
			sender: this.player,
			call: calls.demo.play()
		  }}
		/>
		<Label>Pot Balance
		  <Label.Detail>
			<Pretty value={runtime.demo.pot} />
		  </Label.Detail>
		</Label>
	  </Segment>
	}
  }
```


```
readyRender() {
		return (<div>
			<Heading />
			<WalletSegment />
			<Divider hidden />
			<AddressBookSegment />
			<Divider hidden />
			<FundingSegment />
			<Divider hidden />
			<UpgradeSegment />
			<Divider hidden />
			<PokeSegment />
			<Divider hidden />
			<TransactionsSegment />


			<Divider hidden /> //add this line
    		<DemoSegment />  //add this line
		</div>);
	}
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
