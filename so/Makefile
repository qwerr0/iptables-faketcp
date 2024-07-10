CFLAGS = -Wall -Wextra
LDFLAGS = -lxtables -fPIC -shared

%.so : %.c
	$(CC) $(CFLAGS) $(LDFLAGS) $< -o $@

all: libipt_FAKETCP.so libip6t_FAKETCP.so

clean:
	rm -f *.so

install:
	install -m 755 -t /usr/lib/x86_64-linux-gnu/xtables/ *.so
