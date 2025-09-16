#指定编译器
CC = gcc

#编译选项
CFLAGS = -g -O2 -Wall -Werror  -I./include

# TODO
makeclean.exe: hello.o add.o mul.o
	$(CC) $(CFLAGS) -o makeclean.exe hello.o add.o mul.o

hello.o: hello.c ./include/hello.h ./include/add.h ./include/mul.h
	$(CC) $(CFLAGS) -c hello.c
add.o: ./lib/add.c ./include/add.h ./include/hello.h 
	$(CC) $(CFLAGS) -c ./lib/add.c
mul.o: ./lib/mul.c ./include/mul.h ./include/hello.h
	$(CC) $(CFLAGS) -c ./lib/mul.c

clean:
	rm -f  hello.o ./lib/add.o ./lib/mul.o
