lossless storage graphics codifier

to attempt to do a grid over 8x8 Y and U and V and store the 64 possible different values of Y on a tablepointer that the max value its 1 to 64 and generecly only 11 values are different
then point to that value like 10 and it may means a x1 a y1 of 3 and 4 and store the abs diference of the target y value and that x and y value like the min possible for instances 6
but if the abs its 6 then we need to know if its 6 higher or lower that it comes the abs pointo zero or 1 to say 6 high or six low
we stor that for each pixel and also do the U and V cicles
after all the file becomes not 24 bits a pixel but 17x3 a pixel in the dat file
the trick its that can be highly compressed for instances with emma lea in order to become less size than the lossless bmp.lea or even avif...
this dat.lea file if can be restored to bmp again can be a good trick for lossless compression ...
for now its just test test test...
the dat.nz files are quite quick to do like a bmp file of 2.5Mb can in 4 seconds go to 200Kb lossless over just 4 seconds on my single processor of i5 i dont even use the multithreading

im trying to get compression values just like jpg but its not a look a like photo its the lossless photo no bit taken or changed --- let us see.

one thing i denote that may have failed on the code its i putted a lea file of 3.900 Kb raw inside a bmp 8 bits bmp and i triyed to convert to dat...
even if it was lossless it should not compress the dat file to 2.400kb or less since that result could for us to see as that we are losing data since recursive compression of a lea to a bmp raw with lea should not 
compress it raw binary file of lea already...
if recursive compression its impossible and we are compressing a bmp with lea compressed data it means the y u v are not totally reversible as lossless.
