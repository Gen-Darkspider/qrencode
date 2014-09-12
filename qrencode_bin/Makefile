EXENAME=qrencode
TOOLCHAINPATH=/home/bob/work_tcl/novatekoss/gcc-nt667_linux/bin/
LD_LIB_PATH :=./libs

LDLIB = -L$(LD_LIB_PATH) -lz -lqrencode -lpng15
#libqrencode.a libpng15.so libz.so

CFLAGS=-I ./include

CC=$(TOOLCHAINPATH)arm-linux-gnueabihf-gcc

#LDFLAGS+=-pthread

all: Qrencode

Qrencode: qrenc.o
	$(CC) -o $(EXENAME) qrenc.o $(LDLIB)
	#$(CC) -o $(EXENAME) qrenc.o $(LDFLAGS) $(LIBS)

qrenc.o:
	$(CC) -c $(CFLAGS) qrenc.c


#ROOT := /home/bob
#LD_LIB_PATH :=./libs
#DIR_PATH := ./include
#TARGET = qrencode
#SRC := ./src/qrenc.c
#INC_DIR = -I$(DIR_PATH)

#LDLIB = -L$(LD_LIB_PATH) -lz -lqrencode -lpng15

#$(TARGET) : $(SRC)
#	$(CC) -o $@ $^ $(LDLIB) $(INC_DIR)

clean:
	rm -f *.o
	rm -f *.a
	rm -rf $(EXENAME)