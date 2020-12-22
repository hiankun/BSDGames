CC = gcc
CFLAGS = -Wall -Wno-comment
LIBS = -ltermcap

objects = input.o scores.o screen.o shapes.o tetris.o

all: tetris

tetris: $(objects)
	#$(CC) $? $(CFLAGS) $(LIBS) -o $@
	$(CC) $(CFLAGS) $(objects) $(LIBS) -o $@

tetris.o: tetris.c input.h scores.h screen.h tetris.h
	$(CC) $(CFLAGS) -c tetris.c 

input.o: input.c input.h tetris.h
	$(CC) $(CFLAGS) -c input.c 

scores.o: scores.c pathnames.h scores.h screen.h tetris.h
	$(CC) $(CFLAGS) -c scores.c 

screen.o: screen.c screen.h tetris.h
	$(CC) $(CFLAGS) -c screen.c 

shapes.o: shapes.c tetris.h
	$(CC) $(CFLAGS) -c shapes.c 

clean:
	rm -f *.o tetris
