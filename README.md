# 2phaseLockingProtocol
Implement a program that simulates the behavior of the two-phase locking (2PL) protocol for concurrency control
The particular protocol to be implemented will be rigorous 2PL, with the wound-wait method for dealing with deadlock. The input to your program will be a file of transaction operations in a particular sequence. Each line has a single transaction operation. The possible operations are: b (begin transaction), r (read item), w (write item), and e (end transaction). Each operation will be followed by a transaction id that is an integer between 1 and 9.
For r and w operations, an item name follows between parentheses (item names are single letters from A to Z). Two example are given below.

Input:
Examples of two input files:
b1;                                                                          b1;
r1 (Y);                                                                     r1(Y);
w1 (Y);                                                                    w1(Y);
r1 (Z);                                                                     r1(Z);
b3;                                                                          b2;
r3 (X);                                                                     r2(Y);
w3 (X);                                                                   b3;
w1 (Z);                                                                    r3(Z);
e1;                                                                          w1(Z);
r3 (Y);                                                                     e1;
b2;                                                                          w3(Z);
r2 (Z);                                                                     e3;
w2 (Z);                                                                   
w3 (Y);
e3;
r2 (X);
w2 (X);
e2;
 
