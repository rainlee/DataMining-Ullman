ver=REFINE

objects=seperator.o ullman_init.o ullman_utils.o main.o ullman_query.o\
	   	ullman_build.o graph.o\

ifeq ($(ver), REFINE)
all: ullman
CXXFLAGS= -c -O3 -DREFINE
else
all: ullman
CXXFLAGS= -c -O3
endif

ullman : $(objects)
	g++ -o ullman $(objects) -pg -O2

ullman2 : $(objects)
	g++ -o ullman2 $(objects) -pg -O2

seperator.o : seperator.h
graph.o : graph.h
ullman_build.o : ullman.h
ullman_utils.o : ullman_utils.h
ullman_init.o : ullman.h
ullman_query.o : ullman.h
main.o : common.h ullman.h ullman_utils.h

.PHONY : clean all

clean :
	rm -rf $(objects) ullman
