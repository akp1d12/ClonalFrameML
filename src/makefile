# Make file for ClonalFrameML
CC = g++
CFLAGS += -O3 -I./ -I./myutils -I./coalesce
OBJECTS = main.o
HEADERS = main.h brent.h powell.h version.h

.PHONY: clean version

all: version ClonalFrameML

ClonalFrameML: $(OBJECTS)
	$(CC) $(LDFLAGS) -o ClonalFrameML $(OBJECTS)

main.o: main.cpp $(HEADERS)
	$(CC) $(CFLAGS) -c -o main.o main.cpp

version:
	/bin/echo "#define ClonalFrameML_GITRevision \"`git describe --tags`\"" > version.h

clean:
	rm -f $(OBJECTS)
