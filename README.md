We started with the starter code. This proved to be one of our biggest struggles. After understanding how the two
programs wrote to STDOUT and read from STDIN, we were able to gain a grasp on the protocol.

We were able to identify that the protocol was incorrectly ordering packets, dropping packets, and timing out
in certain situations. The main way we solved these problems was by identifying it either on either the receiver, or the sender side.
Then we would address the problem and make the other side aware of the changes. For example, when ACK packets were being dropped, 
we made the receiver aware of this by sending a 'resend' flag. This allowed the receiver to know it was getting a previously known packet.

We tested our code using the testing scripts along with our own combinations of testing parameters. One of the most used
parameters were TIMEOUT and DROP. This allowed us to test our programs in unforgiving situations.   