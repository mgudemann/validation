
DIR=../Sources
FILETYPE= c

# make sure that the BOOST libraries (in particular dynamic_bitset) is in the include path
CPPFLAGS += -I. -I$(DIR)
CXXFLAGS = -Wall -pedantic -std=c++11
CFLAGS = -Wall -pedantic -std=c11

vpath %.$(FILETYPE)  $(DIR)

all: test_bitwalker FORCE
	./test_bitwalker

test_bitwalker:    test_bitwalker.o Bitwalker.o
	$(CXX) -o $@ $+


format:
	@astyle -A1 -f -p -Y -z2 -c --indent=spaces -s4  *.cpp

clean:
	@$(RM) test_bitwalker
	@$(RM) *.o
	@$(RM) *.orig

FORCE:

