# random_autokey
A program for enciphering messages that contain A-Z and period(.).

works by assigning the usable characters a 3 digit ternary number (Trit) and assigning 81 characters in
total a 4 trit character. It places the letters of the message in a group of four plus a random character
from the larger in to a sixteen trit number it then performs ternary addition on this group to obtain a
different set of sixteen that becomes four characters from the larger table. the random figure becomes
the key for the next group. deciphering reverses the proccess. some will not be stripped from the message,
but instead replaced with a set of usable characters i.e. "!" becomes: ".E." the deciphering function
reverses this automaticaly.

the program uses argparse and can be called in the terminal.
It takes one positional argument that it uses to scramble the larger table. the table is scrambled using the
default python random module so that it can be "seeded" with the keyword to ensure that you have the proper
table when you encipher or decipher. Using a wrong initial key may still produce legible results The algorithm
used cannot fix this.
