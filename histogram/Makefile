#----- Modify CC and CFLAGS as appropriate in your environment
CC = gcc
CFLAGS = -O3 -fopenmp

LIB = -lm -lc

UNITFILES = 

#------------ EXECUTABLE FILES ---------------

all: histo histo_locks histo_atomic histo_creative histo_creative2
histo : histo.o $(UNITFILES)
	$(CC) $(CFLAGS) -o histo histo.o $(UNITFILES) $(LIB)

clean:
	rm -f histo *.o histo_locks *.o histo_atomic *.o histo_creative *.o 

histo.o : histo.c
	$(CC) $(CFLAGS) -c histo.c $(INCLUDE) 

histo_locks : histo_locks.c
	$(CC) $(CFLAGS) -o histo_locks histo_locks.c $(INCLUDE)

histo_atomic : histo_atomic.c
	$(CC) $(CFLAGS) -o histo_atomic histo_atomic.c $(INCLUDE)

histo_creative : histo_creative.c
	$(CC) $(CFLAGS) -o histo_creative histo_creative.c $(INCLUDE)

histo_creative2 : histo_creative2.c
	$(CC) $(CFLAGS) -o histo_creative2 histo_creative2.c $(INCLUDE)
