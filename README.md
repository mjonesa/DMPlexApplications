DMPlexApplications
==================

 Configure options (Ubuntu 12.04):

  apt-get install libnetcdf-dev
  apt-get install libhdf5-serial-dev
  apt-get install libexodusii-dev libexodusii5


./config/configure.py --download-ctetgen  --download-triangle --prefix=/home/mjonesa/local --with-blas-lapack-lib="[/opt/apps/EPD/epd-7.3-1-rh5-x86_64/lib/libmkl_rt.so,/opt/apps/EPD/epd-7.3-1-rh5-x86_64/lib/libmkl_intel_thread.so,/opt/apps/EPD/epd-7.3-1-rh5-x86_64/lib/libmkl_core.so,/opt/apps/EPD/epd-7.3-1-rh5-x86_64/lib/libiomp5.so]"  PETSC_ARCH=arch-linux2-c-debug --debug=1 --with-exodusii-lib="[/usr/lib/x86_64-linux-gnu/libexoIIv2.so]" --with-netcdf-dir=/usr/lib --with-hdf5-dir=/usr/lib --with-c2html=0 --with-exodusii-include=/usr/include


------------ Create Tags -----------
ctags -R --langmap=c++:+.tpp --langmap=c++:+.cu --langmap=c++:+.cl --language-force=c++ $PETSC_DIR



------------ Execute with box mesh ------------

./tcaSolver -run_type test -dim 3 -refinement_limit 0.0125 -variable_coefficient field    -interpolate 1 -petscspace_order 2 -show_initial -dm_plex_print_fem


------------ Execute with exodus file ------------
./tcaSolver -run_type test -dim 3 -variable_coefficient field    -interpolate 1 -petscspace_order 2 -show_initial -dm_plex_print_fem -f LaserModel/meshTemplateFull1.e


------------ Debug ------------
gdb --args ./tcaSolver -run_type test -dim 3 -refinement_limit 0.0125 -variable_coefficient field    -interpolate 1 -petscspace_order 2 -show_initial -dm_plex_print_fem


regular expression break point: 
           rbreak ^f0


------------ Useful Commands ------------

cntl V -> arrows    : visual block

yy  - copy
7yy - copy  7  lines:
9yy - copy  9  lines:
21yy- copy  21 lines:

p   - paste

search backward : 3


esc  exits writ mode

:w  saves

cntl w  - j/k  up/down



-----------------   git commands ----------------

save locally: git commit

push to github: git push -u


----------------- screen ----------------

esckey = cntl e
esckey S  : split screen
esckey |  : vertical split screen

