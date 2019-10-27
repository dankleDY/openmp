#----- Modify CC and CFLAGS as appropriate in your environment
CC = gcc
CFLAGS = -O3 -fopenmp

LIB = -lm -lc

UNITFILES = 

#------------ EXECUTABLE FILES ---------------

all: histo histo_lock
histo : histo.o $(UNITFILES)
	$(CC) $(CFLAGS) -o histo histo.o $(UNITFILES) $(LIB)

clean:
	rm -f histo *.o histo_lock *.o

histo.o : histo.c
	$(CC) $(CFLAGS) -c histo.c $(INCLUDE) 

histo_locks : histo_locks.c
	$(CC) $(CFLAGS) -o histo_locks histo_locks.c $(INCLUDE)

histo_atomic : histo_atomic.c
	$(CC) $(CFLAGS) -o histo_atomic histo_atomic.c $(INCLUDE)
