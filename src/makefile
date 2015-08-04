CC=g++
CPPFLAGS=-I. -lstdc++ -lpthread -lrt -lwiringPi
DEPS = commands.h config.h events.h si4703.h xbmcclient_if.h common.h event-server.hradio.h xbmcclient.h
OBJ = main.o commands.o event-server.o radio.o xbmcclient_if.o events.o si4703.o

%.o: %.cpp $(DEPS)
	$(CC) -c -o $@ $< $(CPPFLAGS)

carpc-controller: $(OBJ)
	$(CC) -o $@ $^ $(CPPFLAGS)
