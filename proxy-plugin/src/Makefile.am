include $(top_srcdir)/config/utility.am

lib_LTLIBRARIES = libsipxcustomcallerid.la

## Libtool version info - update only immediately before a release
# Current - increment if any interfaces are added, removed, or changed
version_Current = 1

# Revision - set to 0 if Current was incremented
#            increment if any implementation has changed
version_Revision = 0

# Age - set to 0 of any interfaces have been removed
#       increment if any interfaces have been added
version_Age = 0

libsipxcustomcallerid_la_LDFLAGS = \
	-module \
	-version-info ${version_Current}:${version_Revision}:${version_Age}

libsipxcustomcallerid_la_LIBADD = \
	@SIPXCOMMSERVER_LIBS@

libsipxcustomcallerid_la_SOURCES = \
	CallerID.cpp \
	CallerID.h

TESTS = CallerMongoDBTest

check_PROGRAMS = $(TESTS)

TEST_LIBS =  \
	@SIPXUNIT_LIBS@ \
	@SIPXCOMMSERVER_LIBS@ \
	$(libdir)/libsipXproxy.la \
	libsipxcustomcallerid.la

CallerMongoDBTest_LDADD = $(TEST_LIBS)
CallerMongoDBTest_SOURCES = CallerMongoDBTest.cpp
