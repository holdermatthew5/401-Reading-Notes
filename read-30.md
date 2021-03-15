# Hash Tables

Hash(data) gives index of the list the data is in (which explains why we added linked lists to the indices of a list in the hash class in the lecture and means that the list isn't a normal list it's a linked list).
Hash - A hash is the result of some algorithm taking an incoming string and converting it into a value that could be used for either security or some other purpose. In the case of a hashtable, it is used to determine the index of the array.
Buckets - A bucket is what is contained in each index of the array of the hashtable. Each index is a bucket. An index could potentially contain multiple key/value pairs if a collision occurs.
Collisions - A collision is what happens when more than one key gets hashed to the same location of the hashtable.
Each index contains a key value pair in the form of a string and seperated by a colon ("key:value").
Adding a key to the value of the node gives it an index to help identify it.
The Hash is the modulo of the sum of number values assigned to a given key for the "key:value" pair.
store(): calculates hash of a key and places the key value pair in the linked list representing a bucket at the hash index of the hash table (`hash_table[hash]`).
read(): calculates hash of a given key and retrieves the key from the 'bucket' at `hash_table[hash]`.
# This looks like what was in the lecture
add() - adds "key:value" pair to hash table.
- sends key to GetHash method
- receives index in which to place "key:value" pair
- check if a linked list is present (assuming hash table is not made with linked lists already in place before values are added)
- if linked list is present add "key:value" pair to the linked list
- else add a linked list then add "key:value" pair to that linked list.
find() - finds the value assigned to a key in a hash table.
- sends key to GetHash method
- recieves index in which to search for "key" of the "key:value" pair
- retrieves the "value" of the "key:value" pair from the linked list at that index
contains() - returns boolean value declaring whether or not the "key" is present in the hash table.
GetHash() - recieves a "key" and returns the modulo of the sum of the ascii numbers of each character in the "key" string and the length of the list as the index at which to find a bucket/linked-list