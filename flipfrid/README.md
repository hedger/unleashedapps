# Flipfrid

Basic LFRFID Fuzzer.

## Why

Flipfrid is a simple Rfid fuzzer using lfrfid protocols (125khz).
Objective is to provide a simple to use fuzzer to test readers by emulating various cards.

- EM4100 cards use a 1 byte customer id and 4 bytes card id. 
- HIDProx cards use a 2 byte customer id and 3 byte card id.

## How

1) Select the Protocol with the left and right arrows
2) Select the Mode with the up and down arrows
3) Set TD (Time delay) between ID switch if you need, or left it as is
4) Click Start

### Info 

There are 4 Protocols:
- EM4100
- HIDProx
- PAC/Stanley
- H10301

There are 4 modes:
- Default Values: Try factory/default keys and emulate one after the other.
- BF customer id: An iteration from 0X00 to 0XFF on the first byte.
- Load Dump file: Load an existing dump (.rfid) generated by Flipperzero, select an index and bruteforce from 0X00 to 0XFF;
- Uids list: Iterate over an input text file (one uid per line) and emulate one after the other.


TODO : 
- Add second byte test to `BF customer id`
