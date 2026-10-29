#Opgave 1

The reason why it's returning vertical points is because the integer in the line;
new Random().nextInt(maxValue); only returns 0 when the max value is 1.

To fix it, we rewrite the code to;
return new Random().nextInt(maxValue + 1);


#Opgave 2
We never get the message because of this line;
return hitCount > BATTLESHIP_LENGTH;

Even when the hitcounts hit 3, it keeps going since the hitcount has to be bigger
then the battleship length, which itself is 3.

So we should change it to; return hitCount >= BATTLESHIP_LENGTH;



#Opgave 3
Because the endpoints are not in boundary, because the maximum index for the array
is going to be 9 not 10. So when in the game, throws 10, the bug occurs.