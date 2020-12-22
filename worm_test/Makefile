CC = gcc
CFLAGS = -Wall -Wno-comment
LIBS = -lcurses

objects = worm.o

all: worm

worm: $(objects)
	$(CC) $(CFLAGS) $(objects) $(LIBS) -o $@

worm.o: worm.c
	$(CC) $(CFLAGS) -c worm.c 

clean:
	rm -f *.o worm
