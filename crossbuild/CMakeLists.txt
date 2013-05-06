# CMake build for CompilerRT.
#
project(CompilerRT)
# The CompilerRT build system requires CMake version 2.8.8 or higher in order
# to use its support for building convenience "libraries" as a collection of
# .o files. This is particularly useful in producing larger, more complex
# runtime libraries.
cmake_minimum_required(VERSION 2.8.8)


set(GENERIC_SOURCES
  ../lib/absvdi2.c
  ../lib/absvsi2.c
  ../lib/absvti2.c
  ../lib/adddf3.c
  ../lib/addsf3.c
  ../lib/addvdi3.c
  ../lib/addvsi3.c
  ../lib/addvti3.c
  ../lib/apple_versioning.c
  ../lib/ashldi3.c
  ../lib/ashlti3.c
  ../lib/ashrdi3.c
  ../lib/ashrti3.c
  ../lib/clear_cache.c
  ../lib/clzdi2.c
  ../lib/clzsi2.c
  ../lib/clzti2.c
  ../lib/cmpdi2.c
  ../lib/cmpti2.c
  ../lib/comparedf2.c
  ../lib/comparesf2.c
  ../lib/ctzdi2.c
  ../lib/ctzsi2.c
  ../lib/ctzti2.c
  ../lib/divdc3.c
  ../lib/divdf3.c
  ../lib/divdi3.c
  ../lib/divmoddi4.c
  ../lib/divmodsi4.c
  ../lib/divsc3.c
  ../lib/divsf3.c
  ../lib/divsi3.c
  ../lib/divti3.c
  ../lib/divxc3.c
  ../lib/enable_execute_stack.c
  ../lib/eprintf.c
  ../lib/extendsfdf2.c
  ../lib/ffsdi2.c
  ../lib/ffsti2.c
  ../lib/fixdfdi.c
  ../lib/fixdfsi.c
  ../lib/fixdfti.c
  ../lib/fixsfdi.c
  ../lib/fixsfsi.c
  ../lib/fixsfti.c
  ../lib/fixunsdfdi.c
  ../lib/fixunsdfsi.c
  ../lib/fixunsdfti.c
  ../lib/fixunssfdi.c
  ../lib/fixunssfsi.c
  ../lib/fixunssfti.c
  ../lib/fixunsxfdi.c
  ../lib/fixunsxfsi.c
  ../lib/fixunsxfti.c
  ../lib/fixxfdi.c
  ../lib/fixxfti.c
  ../lib/floatdidf.c
  ../lib/floatdisf.c
  ../lib/floatdixf.c
  ../lib/floatsidf.c
  ../lib/floatsisf.c
  ../lib/floattidf.c
  ../lib/floattisf.c
  ../lib/floattixf.c
  ../lib/floatundidf.c
  ../lib/floatundisf.c
  ../lib/floatundixf.c
  ../lib/floatunsidf.c
  ../lib/floatunsisf.c
  ../lib/floatuntidf.c
  ../lib/floatuntisf.c
  ../lib/floatuntixf.c
  ../lib/gcc_personality_v0.c
  ../lib/int_util.c
  ../lib/lshrdi3.c
  ../lib/lshrti3.c
  ../lib/moddi3.c
  ../lib/modsi3.c
  ../lib/modti3.c
  ../lib/muldc3.c
  ../lib/muldf3.c
  ../lib/muldi3.c
  ../lib/mulodi4.c
  ../lib/mulosi4.c
  ../lib/muloti4.c
  ../lib/mulsc3.c
  ../lib/mulsf3.c
  ../lib/multi3.c
  ../lib/mulvdi3.c
  ../lib/mulvsi3.c
  ../lib/mulvti3.c
  ../lib/mulxc3.c
  ../lib/negdf2.c
  ../lib/negdi2.c
  ../lib/negsf2.c
  ../lib/negti2.c
  ../lib/negvdi2.c
  ../lib/negvsi2.c
  ../lib/negvti2.c
  ../lib/paritydi2.c
  ../lib/paritysi2.c
  ../lib/parityti2.c
  ../lib/popcountdi2.c
  ../lib/popcountsi2.c
  ../lib/popcountti2.c
  ../lib/powidf2.c
  ../lib/powisf2.c
  ../lib/powitf2.c
  ../lib/powixf2.c
  ../lib/subdf3.c
  ../lib/subsf3.c
  ../lib/subvdi3.c
  ../lib/subvsi3.c
  ../lib/subvti3.c
  ../lib/trampoline_setup.c
  ../lib/truncdfsf2.c
  ../lib/ucmpdi2.c
  ../lib/ucmpti2.c
  ../lib/udivdi3.c
  ../lib/udivmoddi4.c
  ../lib/udivmodsi4.c
  ../lib/udivmodti4.c
  ../lib/udivsi3.c
  ../lib/udivti3.c
  ../lib/umoddi3.c
  ../lib/umodsi3.c
  ../lib/umodti3.c
  )
add_library(CompilerRT-static STATIC ${GENERIC_SOURCES})
set_target_properties(CompilerRT-static PROPERTIES
                      OUTPUT_NAME "CompilerRT"
                     )

install(TARGETS CompilerRT-static
  ARCHIVE DESTINATION lib
  )
