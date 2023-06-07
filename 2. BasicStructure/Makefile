# TARGETS
build: my_lib.o main.o
	g++ my_lib.o main.o -o main
my_lib.0:
	g++ my_lib.cpp -c
main.o:
	g++ main.cpp -c

execute:
	./main

clear:
	rm -rf *.o
	rm -r main