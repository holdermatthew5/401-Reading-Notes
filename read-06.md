## Linked Lists

It seems to me like a node is only capable of referencing the nodes before and after it.

How do I actually create a node and what is it used for?

It seems like a node can be referenced by name. so is a node an object? is it created similarly?

Does Current.previous.next exist? and does it reference the "next" reference of the previous node? AKA can i set Current.previous.next = Current to plug in a new node before the Current node?

ACTUAL CODE WOULD PROBABLY CLARIFY THIS--> For printing nodes why can't we just print the whole linked list by name instead of iterating through the whole list? Does it just not have the "middleware" for that (I'm sure that's not what middleware is but you get my point)?

Is node just the generic term for things like objects, variables, lists (things that have properties/methods) and we've just been calling these things objects because that's the most closely related data structure we're familiar with and that just makes it easier to reference and understand for instructional purposes? If so would a linked list be able to carry any type?In talking about linked lists are we trying to get into the "code" that's more closely related to binary and less closely related to something like JavaScript?

Arrays require all used memory to be in the same place relative to each other while linked lists can reference nodes that exist anywhere in memory as long as the node has a reference point in that linked list. So is a linked list only a definition of an abstract idea of connection?