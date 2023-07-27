# Batcher-Banyan-Network

Batcher-Banyan networks are a type of multistage interconnection network that is commonly found in multiprocessor interconnections and ATM switches.

A Banyan network could potentially transport data packets from any input to any output, but conflicts at any intermediate state would result in the loss of packets being carried through. To avoid packet loss in the delta network, we sort the data first before delivering it to the banyan(delta) network, which then discovers and routes each packet correctly.

![image](https://github.com/Alagesan-Sushmitha/Batcher-Banyan-Network/assets/137837229/b91779d9-dbfd-4264-8e87-13cec7ce6e93)

## Logic Explanation

* The number of inputs is obtained from the user and random numbers are generated for the given count
* This input first passes through the batcher network, which arranges the data according to the banyan network's desired positions. Then the sorted data is displayed.
* Determine each data's binary values . For each binary value, a column state is generated
* Implement a switching pattern at each column state A|B|C|D to determine the route that each packet will follow, for example, if the packet is 4 ==> 0100, 4 will first travel to A5, as shown in the figure above, from A5 if the first value of binary is 0, go to B1, otherwise B5.
* Similarly, we verify the binary value (0100 - 2nd column) from B1 and move to c1 if value is 0, otherwise C3 in this manner, here it moves to C3 due to 1, then from c3 to D3 then out 4 .We will be able to reach the destination output port appropriately once we have traversed all the switches.
* considering high value 15(1111) all the columns choose to take the down path because of 1 . so the route will be A8 to B8 to C8 to D8 and finally out 15

### Expected Result
![image](https://github.com/Alagesan-Sushmitha/Batcher-Banyan-Network/assets/137837229/7c78acf6-4c4c-499b-ada9-2037affebb79)

## Algorithmic Explanation
*	A random function in Python is invoked in this block of code to generate random integers. 
* Bin() converts the decimal number created at random to binary, yielding the binary corresponding string. 
* This function separates all binary integers digit by digit if provided n bits of binary numbers.
* The digits are sent to a specific slot in the banyan network in this block of code. 
*	The binary numbers are 0's and 1's; if 0's, the top portion of the routing network is mapped to it. 
*	If it's a 1, it'll be assigned to the bottom of the routing network. 
*	Each bit is represented as each column in the Batcher-Banyan network, and here we have four bits that are divided into four columns: A, B, C, and D.
*	The check for batcher banyan 16x16 or 8x8 which is banyan press is also done here
*	In this section of code, the number is chosen from 1 to range+1, as the range begins at 0; the user's input number is retrieved; the number entered must be within the range indicated; random numbers are generated for the given number of input counts. 
*	This is accomplished by importing random libraries, and then storing the resulting random numbers in the array random arr[]. 
*	The random numbers in the array are then printed. 
*	The integers in the array are sorted to avoid packet loss or collision.
*	If the batcher-Banyan network is selected, the for loop runs until all of the random integers in the array are routed to a certain output. 
*	The input numbers are converted to binary using the deci_to_binary function, and the routing is done using the banyan function.

## Working of simulation for the inputs 0-7

![image](https://github.com/Alagesan-Sushmitha/Batcher-Banyan-Network/assets/137837229/faf561df-790e-48a2-9860-0068bdc39476)

![image](https://github.com/Alagesan-Sushmitha/Batcher-Banyan-Network/assets/137837229/ce1c8847-6409-40d8-a3e5-46b9fa912c36)

![image](https://github.com/Alagesan-Sushmitha/Batcher-Banyan-Network/assets/137837229/8c0ad742-6631-470b-a2cd-a9c083de72f3)

### Advantages of this code 
* It accepts up to 16 numbers from the user in a dynamic manner.
* Accepts any input  >= 0 and <= 15
  
## Link to the media file
https://pro.panopto.com/Panopto/Pages/Viewer.aspx?tid=25583167-a590-46b1-8566-ae87005a86ff










