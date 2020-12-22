CC = gcc
CFLAGS = -Wall -Wno-comment
LIBS = -lcurses

objects = worms.o

all: worms

worms: $(objects)
	$(CC) $(CFLAGS) $(objects) $(LIBS) -o $@

worms.o: worms.c
	$(CC) $(CFLAGS) -c worms.c 

clean:
	rm -f *.o worms
