# Batcher-Banyan-Network

Batcher-Banyan networks are a type of multistage interconnection network that is commonly found in multiprocessor interconnections and ATM switches.

A Banyan network could potentially transport data packets from any input to any output, but conflicts at any intermediate state would result in the loss of packets being carried through. To avoid packet loss in the delta network, we sort the data first before delivering it to the banyan(delta) network, which then discovers and routes each packet correctly.

![image](https://github.com/Alagesan-Sushmitha/Batcher-Banyan-Network/assets/137837229/b91779d9-dbfd-4264-8e87-13cec7ce6e93)

## Logic Explanation

1.The number of inputs is obtained from the user and random numbers are generated for the given count
2. This input first passes through the batcher network, which arranges the data according to the banyan network's desired positions. Then the sorted data is displayed.
3. Determine each data's binary values . For each binary value, a column state is generated
4. Implement a switching pattern at each column state A|B|C|D to determine the route that each packet will follow, for example, if the packet is 4 ==> 0100, 4 will first travel to A5, as shown in the figure above, from A5 if the first value of binary is 0, go to B1, otherwise B5.
5. Similarly, we verify the binary value (0100 - 2nd column) from B1 and move to c1 if value is 0, otherwise C3 in this manner, here it moves to C3 due to 1, then from c3 to D3 then out 4 .We will be able to reach the destination output port appropriately once we have traversed all the switches.
6. considering high value 15(1111) all the columns choose to take the down path because of 1 . so the route will be A8 to B8 to C8 to D8 and finally out 15

### Expected Result
![image](https://github.com/Alagesan-Sushmitha/Batcher-Banyan-Network/assets/137837229/7c78acf6-4c4c-499b-ada9-2037affebb79)

## Algorithmic Explanation
•	A random function in Python is invoked in this block of code to generate random integers. 
•	Bin() converts the decimal number created at random to binary, yielding the binary corresponding string. 
•	This function separates all binary integers digit by digit if provided n bits of binary numbers.



