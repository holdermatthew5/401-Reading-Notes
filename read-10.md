## Stacks and Queues

- So then a stack is a singly linked list?
  - **Push** O(1) - Adds node to Top.
  - **Pop** O(1) - Nodes removed from a stack are popped. An exception is raised for an empty stack. Pop takes from Top.
  - **Top** - `.head`?
  - **Peek** O(1) - view node at `.head`? (top). Exception is raised when peek is run on an empty stack.
  - **IsEmpty** O(1) - returns `True` when the stack is empty else `False`.
- So is a stack the same as the CallStack?
- FILO - First In Last Out
  - 1st node added is the last removed.
- LIFO - Last In First Out
  - Last node added is the 1st removed.

### Queue

- What's the difference between a queue and a stack?
  - **Enqueue** O(1) - Nodes or items added to queue.
  - **Dequeue** O(1) - Nodes or items removed from queue.
  - **Front** - First Node/item in a queue.
  - **Rear** - Last Node/item in a queue.
  - **FIFO** - First In First Out
    - First item added is first item removed
  - **LILO** - Last In Last Out
    - Last item added is last item out
