#EXTRA_CFLAGS=-I$(KERNEL_TREE)/drivers/md -I../
UTILS_CFLAGS=-I../

#obj-m += flashcache.o
#flashcache-objs := flashcache_conf.o flashcache_main.o flashcache_subr.o flashcache_ioctl.o

all:
#	make -C $(KERNEL_TREE) M=$(PWD) modules
	$(CC) $(UTILS_CFLAGS) -o flashcache_create flashcache_create.c
	$(CC) $(UTILS_CFLAGS) -o flashcache_destroy flashcache_destroy.c
	$(CC) $(UTILS_CFLAGS) -o flashcache_load flashcache_load.c

install:
	$(INSTALL) -d -m 0755 $(DESTDIR)/usr/sbin
	$(INSTALL) -m 0755 flashcache_{create,destroy,load} $(DESTDIR)/usr/sbin

clean:
#	make -C $(KERNEL_TREE) M=$(PWD) clean
	rm -f flashcache_{create,destroy,load}
