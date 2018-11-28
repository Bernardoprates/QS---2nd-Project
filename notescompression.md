#Huffman Encoding
Storing character in a sequence of 8-bits eficiently is answered by Huffman Encoding with variable-length encoding.
>
The main obstacle that usually poses when using variable-length encoding is being able to decode univoquely, 
and Huffman Encoding solves the problem by following the prefix rule - no codeword is a prefix of another codeword.
> The Huffman Algorithm proceeds as follow:
> * Create leaf nodes for all characters and add them to the priority queue 
(their weight is the absolute frequency of the character)
> * While there is more than one node in the queue:
>   * Remove two nodes of the highest priority from the queue.
>   * Create a new internal node with this two nodes as children and frequency equal to the sum of both.
>   * Add the new node to the priority queue.
> * The remaining node is the root.
>

#LZW 
The LZW method achieves compression by using codes 256 through 4095 to represent sequences of bytes.
>
The codes are stored in a 4096 entries table, and it arises a question of which sequences of characters should be on the table
and how to provide the uncompression program the same table used during the compression.
>
At the begining of the encoding, the table contains only 256 entries filled, corresponding to the codes of the single characters.
As the encoding continues, the LZW algorithm identifies repeated sequences in the data, and adds them to the code table.
Compression starts the second time a sequence is encountered.
>
