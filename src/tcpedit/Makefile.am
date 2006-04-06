noinst_LIBRARIES = libtcpedit.a

libtcpedit_a_SOURCES = tcpedit.c parse_args.c edit_packet.c \
					   rewrite_l2.c portmap.c

manpages: tcpedit.1

tcpedit.1: tcpedit_stub.def
	@AUTOGEN@  -T agman1.tpl --base-name tcpedit tcpedit_stub.def

tcpedit_stub.h: tcpedit_opts.def
	@AUTOGEN@ tcpedit_stub.def

AM_CFLAGS = -I.. -I../common -I../.. 

noinst_HEADERS = tcpedit.h edit_packet.h rewrite_l2.h portmap.h \
				 tcpedit_stub.h parse_args.h

MOSTLYCLEANFILES = *~

MAINTAINERCLEANFILES = Makefile.in