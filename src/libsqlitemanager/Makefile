OBJECTS = $(shell ./getobjname.sh)
CC = gcc
CFLAGS = -isysroot /var/mobile/sysroot \
	 -Wall \
	 -std=gnu99 \
	 -c \
	 -I.. \
	 -I../Categories \
	 -I../Crypto \
	 -I../DropboxSDK \
	 -I../FBConnect \
	 -I../libarchive \
	 -I../libjpeg \
	 -I../libsqlitemanager \
	 -I../MGTwitterEngine \
	 -I../mongoose \
	 -I../MPOAuth \
	 -I../OAuthConsumer \
	 -I../SAOAuthTwitterEngine \
	 -I../SBJSON \
	 -I../TouchJSON \
	 -DTARGET_OS_IPHONE=1 \
	 -DUSE_LIBXML=1 \
	 -DTOUCHJSON_AVAILABLE=1

all: ${OBJECTS}

%.o: %.c
	${CC} ${CFLAGS} -o $@ $^

%.o: %.m
	${CC} ${CFLAGS} -o $@ $^

clean:
	rm -rf ${OBJECTS}

