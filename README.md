## Seismic image processing for geologic faults

This repository contains computer programs written and used by 
[Dave Hale](http://inside.mines.edu/~dhale) 
to create examples shown in his SEG/AAPG Distinguished Lecture in Fall 2014,
entitled 
[3D seismic image processing for interpretation of faults and horizons]
(http://www.seg.org/education/lectures-courses/distinguished-lecturers/fall2014/hale-abstract).

This software depends on that in the [Mines Java
Toolkit](https://github.com/dhale/jtk/). If you want to do more than browse
the source code, you must first download and build the Mines JTK. The build
process (using [Gradle](http://www.gradle.org) ) for this repository is the
same.

Like the Mines JTK, this software is a toolkit for computer programmers. It is
not a complete system for seismic interpretation of geologic faults. Others
(including commercial software companies) have built such systems using
earlier versions of one or more of the software tools provided in this
repository.

### Summary

FaultScanner
: creates images of fault likelihood, strike and dip. This class can also
smooth seismic images along reflectors, while enhancing discontinuities at
faults. The computationally efficient scan over fault strikes and dips has
made an earlier version of this class the most widely used component in this
repository.

FaultSkinner (new in 2014)
: constructs fault skins comprised of fault cells. A fault cell is a point
located on a fault, with an associated fault likelihood, strike and dip. A
fault skin is a linked collection of fault cells used to walk within a seismic
image, up and down along fault curves (tangent to fault dip) and left and
right along fault traces (tangent to fault strike). A fault skin is a
fit-for-purpose representation of a fault that is simpler than a surface mesh.

FaultSlipper (new in 2014)
: uses differences between samples of seismic images on opposite sides of
fault skins to estimate fault dip slips. (Does not estimate strike slips.)
Also includes methods to construct a complete field of fault dip-slip vectors,
and to use those vectors to undo faulting apparent in a seismic image.

FakeData (new in 2014)
: generates synthetic seismic images useful for research and testing.

---
Copyright (c) 2014, Dave Hale. All rights reserved.
This software and accompanying materials are made available under the terms of
the [Common Public License - v1.0](http://www.eclipse.org/legal/cpl-v10.html),
which accompanies this distribution.