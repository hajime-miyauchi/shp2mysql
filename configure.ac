#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.69])
AC_INIT([shp2mysql], [0.3], [hajime.miyauchi@gmail.com])
AM_INIT_AUTOMAKE([foreign])
# AC_CONFIG_SRCDIR([postgis_config.h.in])
AC_CONFIG_HEADERS([config.h])
AM_PROG_LIBTOOL
LT_INIT

# Checks for programs.
AC_PROG_CXX
AC_PROG_AWK
AC_PROG_CC
AC_PROG_CPP
AC_PROG_INSTALL
AC_PROG_LN_S
AC_PROG_MAKE_SET
AC_PROG_RANLIB
AC_PROG_LEX
AC_PROG_YACC

# Checks for libraries.
# FIXME: Replace `main' with a function in `-lgeos_c':
# AC_CHECK_LIB([geos_c], [main])
# FIXME: Replace `main' with a function in `-lm':
AC_CHECK_LIB([m], [main])
# FIXME: Replace `main' with a function in `-lproj':
# AC_CHECK_LIB([proj], [main])

# Checks for header files.
AC_FUNC_ALLOCA
AC_CHECK_HEADERS([float.h inttypes.h libintl.h limits.h locale.h malloc.h stddef.h stdint.h stdlib.h string.h unistd.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_C_INLINE
AC_TYPE_INT16_T
AC_TYPE_INT32_T
AC_TYPE_INT64_T
AC_TYPE_INT8_T
AC_TYPE_OFF_T
AC_TYPE_SIZE_T
AC_TYPE_UINT16_T
AC_TYPE_UINT32_T
AC_TYPE_UINT64_T
AC_TYPE_UINT8_T

# Checks for library functions.
AC_FUNC_FSEEKO
AC_FUNC_MALLOC
AC_FUNC_REALLOC
AC_FUNC_STRTOD
AC_CHECK_FUNCS([floor memmove memset modf pow rint setlocale sqrt strcasecmp strchr strcspn strdup strerror strspn strstr strtol])

export ac_cv_func_realloc_0_nonnull=yes
export ac_cv_func_malloc_0_nonnull=yes

AM_GNU_GETTEXT_VERSION([0.19.8])
AM_ICONV

AC_CONFIG_FILES([Makefile
                 liblwgeom/Makefile
                 src/Makefile])
AC_OUTPUT
