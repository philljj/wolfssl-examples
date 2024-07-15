CC=gcc
#if you installed wolfssl to an alternate location use CFLAGS and LIBS to
#control your build:

#EXAMPLE: set WOLFSSL_INSTALL_DIR to point to your install location like so:

# WOLFSSL_INSTALL_DIR=/Users/kalebhimes/work/testDir/wolf-install-dir-for-testing

#END EXAMPLE

WOLFSSL_INSTALL_DIR=/usr/local

# ECC Examples Makefile
CC       = gcc
WOLFSSL_INSTALL_DIR = /usr/local
CFLAGS   = -Wall -I$(WOLFSSL_INSTALL_DIR)/include -DUSE_WOLFSSL
LIBS     = -L$(WOLFSSL_INSTALL_DIR)/lib -lm

# option variables
DYN_LIB         = -lwolfssl
STATIC_LIB      = $(WOLFSSL_INSTALL_DIR)/lib/libwolfssl.a
DEBUG_FLAGS     = -g -DDEBUG
DEBUG_INC_PATHS = -MD
OPTIMIZE        = -Os

# Options
#CFLAGS+=$(DEBUG_FLAGS)
CFLAGS+=$(OPTIMIZE)
#LIBS+=$(STATIC_LIB)
LIBS+=$(DYN_LIB)

all:test_acert

test_acert:test_x509_acert.o
	$(CC) -o $@ $^ $(CFLAGS) $(CPPFLAGS) $(LIBS)

.PHONY: clean all

clean:
	rm -f *.o test_acert
