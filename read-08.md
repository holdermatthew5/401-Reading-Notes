## List Comprehensions

`list_comprehensions = [expression for i in list if conditional]`
  - expression is an item to be appended to the new list
  - i is the index on a given iteration of the for loop
  - list is any iterable datastructure
  - conditional is optional and declares whether or not a given instance of expression will be appended to the new list.
  - Q - Are parenthesis on `expression` required regardless of data structure? Can I replace them with brackets?
  - Q - Why is it safe to use `i` instead of `list[i]` in `multiplied = [item*3 for item in list1]`? Shouldn't I need to use `list1[item]` for the expression? If not why does this not work with a regular for loop?
  - list comprehension works with files by iterating through the file line by line.
  - nest loops by typing the nested loop to the right of the first loop. Do not seperate by more than a space.