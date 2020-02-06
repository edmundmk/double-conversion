project( 'double-conversion', 'cpp', version : '3.1.5' )

headers = [
    'double-conversion/bignum.h',
    'double-conversion/cached-powers.h',
    'double-conversion/diy-fp.h',
    'double-conversion/double-conversion.h',
    'double-conversion/double-to-string.h',
    'double-conversion/fast-dtoa.h',
    'double-conversion/fixed-dtoa.h',
    'double-conversion/ieee.h',
    'double-conversion/string-to-double.h',
    'double-conversion/strtod.h',
    'double-conversion/utils.h'
]

sources = [
    'double-conversion/bignum.cc',
    'double-conversion/bignum-dtoa.cc',
    'double-conversion/cached-powers.cc',
    'double-conversion/double-to-string.cc',
    'double-conversion/fast-dtoa.cc',
    'double-conversion/fixed-dtoa.cc',
    'double-conversion/string-to-double.cc',
    'double-conversion/strtod.cc'
]

cpp_args = [ '-DDOUBLE_CONVERSION_BUILD' ]

double_conversion_lib = library( 'double-conversion', sources : sources, cpp_args : cpp_args, gnu_symbol_visibility : 'hidden', install : true )
double_conversion_lic = files( 'LICENSE' )
double_conversion_dep = declare_dependency( include_directories : include_directories( '.' ), link_with : double_conversion_lib )
install_headers( headers, subdir : 'double-conversion' )
