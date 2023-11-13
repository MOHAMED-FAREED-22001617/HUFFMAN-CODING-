# Huffman-Coding
## Aim
To implement Huffman coding to compress the data using Python.

## Software Required
1. Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>
Assign the input string.

### Step2:
<br>
Create the required tree nodes.

### Step3:
<br>
Create a function to implement the huffman coding.

### Step4:
<br>
Calculate frequency of occurence.

### Step5:
<br>
Print the characters and its Huffman code.
 
## Program:


# Get the input String
``` Python
string = 'string='KRISHNA_212221230052''
```
# Create tree nodes
``` Python
class Nodetree(object):
    def __init__(self,left=None,right=None):
        self.left= left
        self.right =right
    def children(self):
        return(self.left, self.right) 
```

# Main function to implement huffman coding
``` Python

def huffman_coding(Tree,left =True,binString=''):
    if type(Tree) is str:
        return {Tree : binString}
    (l, r) = Tree.children()
    d = dict()
    d.update(huffman_coding(l,True,binString+ '0'))
    d.update(huffman_coding(r,False,binString+ '1'))
    return d

```

# Calculate frequency of occurrence
``` Python
nodes = freq
while len(nodes) >1:
    (key1 , value1 ) = nodes[-1]
    (key2 , value2 ) = nodes[-2]
    nodes = nodes[:-2]
    Tree = Nodetree(key1,key2)
    nodes.append((Tree , value1+value2))
    nodes = sorted(nodes, key =lambda x:x[1],reverse =True)

```

# Print the characters and its huffmancode
``` Python
huffman = huffman_coding(nodes[0][0])
print('character | Huffman code')
print('-------------------------')
for (char , frequency) in freq:
    print(' %-4r | %12s ' %(char, huffman[char]))




```
## Output:

![242225465-4a2b6a75-7969-458b-adc0-5f610cfaa7d5](https://github.com/MOHAMED-FAREED-22001617/HUFFMAN-CODING-/assets/121412904/5928838e-c276-444b-89f5-a3978d09db05)




## Result
Thus the huffman coding was implemented to compress the data using python programming.
