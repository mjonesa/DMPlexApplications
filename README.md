DMPlexApplications
==================


------------ Execute ------------

./tcaSolver -run_type test -dim 3 -refinement_limit 0.0125 -variable_coefficient field    -interpolate 1 -petscspace_order 2 -show_initial -dm_plex_print_fem


------------ Debug ------------
gdb --args ./tcaSolver -run_type test -dim 3 -refinement_limit 0.0125 -variable_coefficient field    -interpolate 1 -petscspace_order 2 -show_initial -dm_plex_print_fem
