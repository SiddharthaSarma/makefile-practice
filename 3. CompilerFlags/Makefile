# VARIABLES
DEBUG = 1
EXECUTABLE_MAIN = main
CXX_VERSION = c++17
CXX = g++
CXXFLAGS = -Wall -Wextra -Wpedantic -std=$(CXX_VERSION)

COMPILER = $(CXX) $(CXXFLAGS)
ifeq ($(DEBUG), 1)
CXXFLAGS += -g -O0
else
CXXFLAGS += -O3
endif

# TARGETS
build: my_lib.o main.o
	$(COMPILER) my_lib.o main.o -o $(EXECUTABLE_MAIN) 
my_lib.o:
	$(COMPILER) my_lib.cpp -c
main.o:
	$(COMPILER) main.cpp -c

execute:
	./$(EXECUTABLE_MAIN)

clear:
	rm -rf *.o
	rm -r $(EXECUTABLE_MAIN)