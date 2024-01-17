FLAGS = -no-pie

all: avalia


avalia: meuAlocador.o avalia.o
	gcc meuAlocador.o avalia.o ${FLAGS} -o avalia

meuAlocador.o: meuAlocador.s
	as meuAlocador.s -o meuAlocador.o -g


avalia.o: avalia.c
	gcc -c avalia.c -o avalia.o

run: all
	./avalia

clean: 
	rm -rf *.o

purge: clean
	rm -rf avalia