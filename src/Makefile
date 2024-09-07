CL := gcc -O3 -Wall -pedantic -std=c99
CC := gcc -O3 -Wall -pedantic -std=c99
BUILD:=.build

all: mkbuilddir lightbig

mkbuilddir:
	mkdir -p ${BUILD}

lightbig:
	${CC} -c lightbig.c -o ${BUILD}/lightbig.o
	${CL} -o ${BUILD}/test test_lightbig.c ${BUILD}/lightbig.o
	${BUILD}/test
