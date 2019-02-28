## Build notice

- After successful compiliation of OpenBabel you _must_ rename the file openbabel-x.y.z/include/openbabel/locale.h to _locale.h otherwise the compiler will barf when compiling pgchem!
- If you build against PostgreSQL 10.x, make sure to adjust the includes for md5.h in molecule_io.c, molecule_gist.c, reaction_io.c, and reaction_gist.c accordingly. md5.h has moved from libpg/md5.h to common/md5.h!
- If you build against PostgreSQL 11.x and get errors regarding uppercase booleans: change them to lowercase in the affected statements
https://github.com/pgpointcloud/pointcloud/pull/237
