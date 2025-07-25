the file that is just compressed like jpg mp3 lea paq8o or etc its readed into memory.
the next step its to create a random table of several iterations in this case 1Mb iterations can be less for more speed
and also on those iterations you produce 64 tryouts pointers to a 1024 blockbits
witch means iteration [5 of  1Mb, and 6 of 64 TRYOUTS] for instances have the pointer number 645 of 1024 BLOCKBITS
the next thing its to read the blockbits of 1024 0 and ones.
then you produce something like for the repeat cicle of each iteration you check in sequencial mode if
its 1 and 0 sequencial you store just 00 2 bits ( this its randomtable [iteration,num1] = 1 and random [iteration,num1]+1= 0 
its 1 and 1 and 0 sequencial you store just 01 2 bits
its 1 and 1 and 1 and 0 you store just 02 2 bits
its 1  and 1 and 1 and 1 you store just 03 2 bits
if its zero it break the pattern can not sequencial compress

denote that num1 and next num1 does not means sequencial bits on blockbits 1024 its pointers to diferent like 645 and 367 or soo but some can overlap no problem
the 64 tryouts generecly are just something you can point like the 14 tryout to 34 tryout of 20 sequencial good tryouts in a specific iteration
it means you extract like 40 bits just of 00 01 02 03 chunks and save the the beginning tryout 6 bits = 64 value and the lenght of tryouts 6 bits = 64 value and the specific seed iteration of random table

but that does not solves the remaining not found zeros and ones of the all 1024 bits..
soo you have to check witch bits are pointed as 10 110 1110 and 1111 and those which are not you save them in row of bitsw2 array for later save

the saving must have first the size of original file into 32 bits integer value
the num of iterations of 1024 blocks also a 32 bits integer value

the 6 bits number of 64 value of all the beginning pointers of tryouts
the 6 bits number of 64 value of all the length of sequencial tryouts

then its the sequencial chunks of just 2 bits each of each numiter

the real 20 bits representing the seednum iterfinal of 1Mb possibilites its also saved for each iteration of 1024 BLOCKBITS

and you save the remaning bitsw2 into the file also (those 0 and 1s you can not compress on 1024 bits) sequencialy.

its should be done but as you know filesizes are not all plain multiple of 128 bytes or of the 1024 bits chunks that we process in steps of each time
soo you save the remaining bytes that shuold be from 127 to 0 bytes.

all saved into the compressed dat file on the compressorv001.bmx

if you execute it converts a sample.jpg file onto a sample.jpg.dat that even with rar can compress to abit more than just jpg.

its should be reverseble.
