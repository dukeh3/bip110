
based on how seqwit was done

add a hash to the op_ret, this hash is a hash of a set of optional userdata to be added in a new chanin extention, included by the miners in a new
section in the blockchain called the userattacheddata section. 

miners that support the feature add two extra checksums to the block.

1. checksum of all of the attached user data in the datablock togetther with whatever.
2. checksum of all of  the outstanding UTXO. 
3. payment for storing userattacheddata in the section is counted as 16 contra regular blockspace. (min 1/sat/byte) 