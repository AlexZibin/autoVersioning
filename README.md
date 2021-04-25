# Automated Version Number Generation
I've just changed (reversed) the verion string from DDMMYY to YYMMDD, prefixed by constant string. This way, we can simply compare 2 versionstrings in php to decide which one is newer.

Everything is defined and setup in build_defs.h and it's pretty much self explanatory: the  **\__DATE__** and **\__TIME__** gcc preprocessor macros are used to build up a unique automated self incrementing version build number that can be used anywhere in a project. The given example includes a ready made const char TimestampedVersion[] definition that will build a version number from runtime project build date/time components that will end up looking like this: **1.140216.2041**
