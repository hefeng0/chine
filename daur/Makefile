
CC=gcc
RE2C=re2c
BISON=bison
TARGET=daur


all:
	${RE2C} -8 -o daur_scanner.c -c -t daur_scanner_def.h daur_scanner.l
	${BISON} -d daur_parser.y 
	${CC} -o ${TARGET} daur_parser.tab.c daur_scanner.c

.PHONY:clean
clean:
	-rm -f ${TARGET}
	-rm -f *.o
	-rm -f daur_scanner_def.h daur_scanner.c daur_parser.tab.*
