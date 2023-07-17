# NAME: Justin Pank
# EMAIL: jtpank@g.ucla.edu
# ID: 204417822 
CC = gcc
CFLAGS = -std=gnu11 -g -Wall -Wextra -Wno-unused-parameter -Wpointer-sign
FILES   = lab1b-server.c lab1b-client.c Makefile README 

all:
	$(CC) $(CFLAGS) lab1b-server.c -lz -o lab1b-server
	$(CC) $(CFLAGS) lab1b-client.c -lz -o lab1b-client
dist: 
	tar -czvf lab1b-204417822.tar.gz $(FILES)
clean:
	rm -f lab1b-server lab1b-client lab1b-204417822.tar.gz 


