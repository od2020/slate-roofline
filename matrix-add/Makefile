CC      = cc 
CFLAGS	= -O2 -Wall -g

INCLUDE_DIR = -I../lib/AriesNCL/src
LIBRARY_DIR = -L../lib/AriesNCL/src
LIBRARIES = -lmpich -lpapi -lariesncl 

all: matrix_add

matrix_add: matrix_add.c
	${CC} ${CFLAGS} matrix_add.c -o matrix_add_aries   ${INCLUDE_DIR} ${LIBRARY_DIR} ${LIBRARIES} -DARIES -DPROFILING
	${CC} ${CFLAGS} matrix_add.c -o matrix_add_advisor -lmpich

clean: 
	rm -f matrix_add_aries matrix_add_advisor

reallyclean:
	rm -f matrix_add_aries matrix_add_advisor *.json *.bin
