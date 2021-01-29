# <3 Vyper

Contract address: https://etherscan.io/address/0x45128CB743951121Fb70cb570c0784492732778A#code

Notice how the beginning of the onchain bytecode is slightly different vs the compiled runtime output, and throughout the bytecode (Vyper 0.2.8):

0x341561000a57600080fd5b600436101561001857613d84565b600035601c5274012a05f1fffffffffffffffffffffffffdabf41c006080527ffffffffffffffffffffffffed5fa0e000000000000000000000000000000000060a...

vs

0x341561000a57600080fd5b600436101561001857613d47565b600035601c52600015610091575b6101805261014052610160526101405161016051808202821582848304141761004e57600080fd5b80905090509050604e60025...

Although the deployment code does match (input data for txn https://etherscan.io/tx/0x60487fb3b248a48531a329997cce8d1794e4716da6226525c7dbdd55dcc4913b, minus the constructor arguments at the end). Does look like the on-chain bytecode is an excerpt of the deployment bytecode, which differs with the runtime bytecode?
