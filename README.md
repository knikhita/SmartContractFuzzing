# Scribble 

We'll use Scribble to annotate it with properties, and use Mythril to automatically check the properties (and find bugs ).


### Installation
```
# We'll use Mythril to automatically test specifications
pip3 install mythril

# Make sure to use node 10-12
npm install eth-scribble --global
npm install truffle --global
npm install -g @truffle/db
npm install ganache-cli --global
```

### Instrumenting Contracts for Fuzzing

```
pip3 install diligence-fuzzing
fuzz arm 
 Run Truffle compile 
 Run Truffle exec scripts/seed.js
fuzz run > this will create campaign in dashbaord
fuzz disarm
```

### Finding the bugs using Mythril (optional)

```
scribble --arm -m files ./CONTRACT-NAME.sol
myth analyze ./contracts/CONTRACT-NAME.sol

# Always clean up after yourself 😉
scribble --disarm -m files ./contracts/CONTRACT-NAME.sol
```
