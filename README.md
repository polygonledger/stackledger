# stackleger

python -m venv stackledger_env
source stackledger_env/bin/activate
git clone https://github.com/vyperlang/vyper
git clone https://github.com/eth-brownie/brownie.git
git clone https://github.com/brownie-mix/react-mix.git

cd vyper && make
vyper --version

PYTHONPATH="/Users/ben/polygon/stackledger/vyper:$PYTHONPATH"
PYTHONPATH="/Users/ben/polygon/stackledger/vyper"
export PYTHONPATH

brownie compile

yarn install
yarn start

## accounts

add a localaccount in console

accounts.add() 

accounts[-1].balance()  

accounts[0].transfer(accounts[-1], "10 ether") 

accounts[-1].private_key 