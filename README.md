## Features
* Engine
  * Bitboard representation
  * Zobrist hashing
* Search
  * Negamax framework
  * Aspiration Window
  * Alpha-Beta pruning
  * Reverse Futility pruning
  * Late-move reduction
  * Late-move pruning
  * Null-move pruning
  * Razoring
  * IIR
  * SE
  * SEE pruning
  * Check extension
  * PVS
  * Quiescence search
  * Transposition Table
  * Repetition detection
  * killer move, history
  * MVV-LVA capture ordering
  
* Evaluation
  * NNUE Evaluation (Big thanks to Luecx)

## Things i might try in the future
* Evaluation
  * Improve the nnue using a better architecture and generating more data
* Search
   * All the histories i don't comprehend at the time of writing (mostly FUH)
* TT
   * Get Buckets working
   
 ## Building

```bash
$ git clone https://github.com/PGG106/Alexandria
$ cd alexandria/src
$ make 
$ ./Alexandria
```
 ## How to use the engine

The Universal Chess Interface (UCI) is a standard protocol used to communicate with
a chess engine, and is the recommended way to do so for typical graphical user interfaces
(GUI) or chess tools. Alexandria implements the majority of its options as described
in [the UCI protocol](https://www.shredderchess.com/download/div/uci.zip).

## Participating in the project

Alexandria's improvement is a time consuming effort and any help is extremely appreciated. 
If you like the project and what to help it out the following are the preferred ways to do so, please read the next section very carefully.

### Donating hardware

If you want to donate hardware that will go towards testing patches for the engine, you can donate
your hardware resources by getting a client file for [OpenBench](https://github.com/AndyGrant/OpenBench)
and creating a profile on alexandria's OB instance [here](https://pgg106.pythonanywhere.com/).

### Improving the code
Alexandria is open to external PRs and code contributions are highly encouraged and appreciated, just abide by a few rules:
#### Issues
1) before starting to work on a PR that fixes an issue with the engine open an issue in the repository first, from that we'll be able to discuss on who will handle the issue and 
what is the best way to proceed in fixing it.
#### Bench altering commits (anything that is functional and changes bench)
1) Please make sure your idea makes sense from a chess engine development point of view, no single position analysis nor bizarre chess theories that only apply to humans.
2) If possible SPRT your change before making the PR, if not create a test on alexandria's OB instance and i'll judge whether i can spare the resources to run it or 
not.

## Acknowledgements
This project would not have been possible without the following people
* BluefeverSoftware for his Vice chess engine from which i learnt the basic structure and functionality of a chess engine
* CodeMonkeyKing for his bbc chess engine from which i learnt how bitboards work and several refined search techniques
* The whole Stockfish Discord server and Disservin in particular for the sharing of code and the avaliability in answering questions
* A giant thanks to Luecx that helped me immensely in the process of setting up the NNUE and gave me some training data generated by Koivisto
* Lucex (again) and Jay Honnold for the wonderlud CudAD trainer that was used to train the NNUE https://github.com/Luecx/CudAD
* Andrew Grant for the OpenBench platform https://github.com/AndyGrant/OpenBench
* Morgan Houppin, author of Stash for his "option" code https://github.com/mhouppin/stash-bot
