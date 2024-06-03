
Last In, First Out

add = push()
remove = pop()

peek() allows you to see the top item

## Applications of a stack:
* word document undo/redo
* back/forwards in a web
* Recursion stack
* can of Pringles

## Linked Stack

idea: Use a singly linkedList as a stack

We can use the front of the linked list as the top of the stack


## Array Stack

Use the back as the top of the stack

## Clear

How to implement clear() method?

LinkedList.clear()
head = null O(1)

ArrayList.clear()
* size=0
* loop through and set each elemtn to null O(1)
* arr = new arr O(1)


In a double ended queue, you can remove and add from front and back.