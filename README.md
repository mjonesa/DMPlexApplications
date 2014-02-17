DMPlexApplications
==================

 Configure options --download-ctetgen --download-f2cblaslapack --download-triangle --prefix=/home/mjonesa/local --with-blas-lapack-lib="[/opt/apps/EPD/epd-7.3-1-rh5-x86_64/lib/libmkl_rt.so,/opt/apps/EPD/epd-7.3-1-rh5-x86_64/lib/libmkl_intel_thread.so,/opt/apps/EPD/epd-7.3-1-rh5-x86_64/lib/libmkl_core.so,/opt/apps/EPD/epd-7.3-1-rh5-x86_64/lib/libiomp5.so]" --with-c2html=0 --with-clanguage=c++ PETSC_ARCH=arch-linux2-cxx-debug --debug=1


------------ Execute ------------

./tcaSolver -run_type test -dim 3 -refinement_limit 0.0125 -variable_coefficient field    -interpolate 1 -petscspace_order 2 -show_initial -dm_plex_print_fem


------------ Debug ------------
gdb --args ./tcaSolver -run_type test -dim 3 -refinement_limit 0.0125 -variable_coefficient field    -interpolate 1 -petscspace_order 2 -show_initial -dm_plex_print_fem


------------ Useful Commands ------------

cntl V -> arrows    : visual block

yy  - copy
7yy - copy  7  lines:
9yy - copy  9  lines:
21yy- copy  21 lines:

p   - paste



esc  exits writ mode

:w  saves

cntl w  - j/k  up/down



-----------------   git commands ----------------

save locally: git commit

push to github: git push -u
