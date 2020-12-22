CC = gcc
CFLAGS = -Wall -Wno-comment
LIBS = -ll -lm -lcurses

objects = extern.o grammar.o graphics.o input.o lex.o \
	 list.o log.o main.o tunable.o update.o

all: atc

atc: $(objects)
	$(CC) $(CFLAGS) $(objects) $(LIBS) -o $@

main.o: main.c include.h pathnames.h
	$(CC) $(CFLAGS) -c main.c 

extern.o: extern.c include.h
	$(CC) $(CFLAGS) -c extern.c 

grammar.o: grammar.c include.h
	$(CC) $(CFLAGS) -c grammar.c 

graphics.o: graphics.c include.h
	$(CC) $(CFLAGS) -c graphics.c 

input.o: input.c include.h pathnames.h
	$(CC) $(CFLAGS) -c input.c 

lex.o: lex.c include.h grammar.h
	$(CC) $(CFLAGS) -c lex.c 

list.o: list.c include.h
	$(CC) $(CFLAGS) -c list.c 

log.o: log.c include.h pathnames.h
	$(CC) $(CFLAGS) -c log.c 

tunable.o: tunable.c
	$(CC) $(CFLAGS) -c tunable.c 

update.o: update.c include.h
	$(CC) $(CFLAGS) -c update.c 

clean:
	rm -f *.o atc
