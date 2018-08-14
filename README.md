# Asia Blockchain Hackathon 2018

[Technical competition]<br>
Hello Developers!<br>
We are gladly hosting Blockchain & A.I. technical competition. You can select one of the following topics and join the competition! (1) Blockchain Dapp competition (2)  Blockchain based credit information application (3) Improving Accuracy of prediction model<br>

Participant who wants to join our technical competition should prepare presentation document & executive summary about what your team prepared.


• The criteria for award: practicality and novelty<br>
• Please refer to our github for getting started with dapp development

Thank you!


# Preparation for Dapp Development
- Ganache<br>
1) Type the following command to install<br>
<code>npm install -g ganache-cli</code><br>
2) Run Ganache-cli<br>
<code>ganache-cli -p 7545</code><br>

- Truffle<br>
1) <code>npm install -g truffle</code><br>
2) Make a new folder and type the next line.<br>
<code>truffle init</code><br>
3) open the folder “migrations” and create a new file named “2_deploy_contracts.js”.
4) 2_deploy_contracts.js should be as follows.
```js
const YourSolidityName = artifacts.require("./YourSolidityName.sol")

module.exports = function(deployer) {
	deployer.deploy(YourSolidityName);
};
```
5) Put this code inside of "truffle-config.js":<br>
```js
module.exports = {
  // See <http://truffleframework.com/docs/advanced/configuration>
  // for more about customizing your Truffle configuration!
  networks: {
    development: {
      host: "127.0.0.1",
      port: 7545,
      network_id: "*" // Match any network id
    }
  }
};
```
6) code your solidity project and deploy with the two commands
```
truffle compile
truffle migrate --network development
```
7) You can test your code at the truffle console
```
truffle console --network development
```

