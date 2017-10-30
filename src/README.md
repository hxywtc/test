Bitcoin Core Hack Record 
=====================================

What Changes?
----------------

Changes to be committed:  
   (use "git reset HEAD <file>..." to unstage)  

       new file:   blockexample.txt  
       new file:   receivedTxExample.txt  
       new file:   src/README.md  

Changes not staged for commit:  
   (use "git add <file>..." to update what will be committed)  
   (use "git checkout -- <file>..." to discard changes in working directory)  

       modified:   src/net_processing.cpp  
       modified:   src/net_processing.h  
       modified:   src/primitives/transaction.cpp  
       modified:   src/validation.cpp  
       modified:   src/validation.h  

You can search "hxywtc" for details in above modified files.  

Functions
-------

1. Can get all the block information of the main chain bottom-up.   
2. Can record the received Tx and the corresponding peer address.  

You can see the examples in blockexample.txt and receivedTxExample.txt.  

How to build?
-------------------

./autogen.sh  
./configure --with-incompatible-bdb --enable-debug  
make  
make install (optional)  

Then ./src/bitcoind is the bitcoin core we changed.  
Use ./src/bitcoind -debug, you can find the log file in ~/.bitcoin/debug.log  
