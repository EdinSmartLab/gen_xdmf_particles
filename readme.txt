gen_xdmf_box.f90 and gen_xdmf_points.f90 generates XDMF files for visualizing a time series of point data with e.g. paraview.
the parameters are set in param.h90 and the files can be generated by running ./genview.sh

analogous routines for 3D Eulerian fields can be found under the folder utils/ of github.com/p-costa/CaNS

the particle data is assumed to be stored in a binary file as follows (n is the number of points):
v1(1),v2(1),v3(1), ..., v1(n),v2(n),v3(n) --> for vector data
s1(1), ..., s1(n)                         --> for scalar data

these are the routines I used for efficiently visualizing O(10^6) spherical particles with point data stored in binary files.

written in Fortran 90 some years ago.

Pedro Costa (p.simoes.costa@gmail.com)
