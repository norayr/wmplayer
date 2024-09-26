CC     = gcc
LIBDIR = -L/usr/X11R6/lib -L/usr/lib
LIBS   = -lXpm -lXext -lX11 -lpthread `pkg-config --libs gtk+-2.0`
CFLAGS = `pkg-config --cflags gtk+-2.0`

OBJS =	wmplayer.o \
	../wmgeneral/wmgeneral.o \
	../wmgeneral/misc.o \
	../wmgeneral/list.o

all: wmplayer
.c.o:
	$(CC) -g -c -O2 -Wall $< -o $*.o $(CFLAGS)

wmplayer: $(OBJS)
	$(CC) -Wall -g -o wmplayer $^ $(LIBDIR) $(LIBS)

install:
	cp wmplayer /usr/local/bin/

clean:
	rm -f wmplayer $(OBJS)
	rm -f wmplayer
