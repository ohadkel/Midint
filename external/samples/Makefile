CC     = g++
#CC     = clang++
CFLAGS = -Wall -pedantic -O2 -I.. -DTTMATH_DONT_USE_WCHAR


.SUFFIXES: .cpp .o

.cpp.o:
	$(CC) -c $(CFLAGS) $<


all: uint int big big2 parser


uint: uint.o
	$(CC) -o uint -s $(CFLAGS) uint.o

int: int.o
	$(CC) -o int -s $(CFLAGS) int.o

big: big.o
	$(CC) -o big -s $(CFLAGS) big.o

big2: big2.o
	$(CC) -o big2 -s $(CFLAGS) big2.o

parser: parser.o
	$(CC) -o parser -s $(CFLAGS) parser.o


uint.o:		uint.cpp
int.o:		int.cpp
big.o:		big.cpp
big2.o:		big2.cpp
parser.o:	parser.cpp


clean:
	rm -f *.o
	rm -f *.s
	rm -f uint
	rm -f int
	rm -f big
	rm -f big2
	rm -f parser
# on MS Windows suffixes .exe will be automatically added
	rm -f *.exe
