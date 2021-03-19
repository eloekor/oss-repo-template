all: myProgram

myProgram: main.o libmylib.a #libmylib.a is the dependency for the executable
        gcc -lm -o myProgram main.o -L. -lmylib

main.o: main.c
        gcc -O -c main.c main.h

addSorted.o: addSorted.c addSorted.h
        gcc -O -c addSorted.c

freeLinks.o: freeLinks.c freeLinks.h
        gcc -O -c freeLinks.c

libmylib.a: addSorted.o freeLinks.o #let's link library files into a static library
        ar rcs libmylib.a addSorted.o freeLinks.o