# Author: Shiva Patel
# File: Makefile
# Last Modified: 2-20-2026
# Purpose: Compiles the entire (all objects) employee program into an executable and has a clean function.

# compiler
CC = g++

# build target executable name
TARGET = employee

# shows compile flags
CFLAGS = -c -Wall -Wextra

# the objects that are being linked into the single executable.
OBJS = main.o Employee.o Officer.o Supervisor.o

# builds the executable which in this case TARGET is just employee with all the objects in it
all: $(TARGET)

# combines all the objects into TARGET (.o) 
$(TARGET): $(OBJS) 
	$(CC) $(OBJS) -o $(TARGET)

# combines each object file
main.o: main.cpp
	$(CC) $(CFLAGS) main.cpp

Employee.o: Employee.cpp Employee.h
	$(CC) $(CFLAGS) Employee.cpp

Officer.o: Officer.cpp Officer.h
	$(CC) $(CFLAGS) Officer.cpp

Supervisor.o: Supervisor.cpp Supervisor.h
	$(CC) $(CFLAGS) Supervisor.cpp

# removes all objects (*.o), Emacs backup (*~), and target.
clean:
	rm -f *.o *~ $(TARGET)