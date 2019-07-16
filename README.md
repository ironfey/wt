# wt
 Learning the wt framework with cmake

Generating Visual Studio Solution
---------------------------------
`cmake -G "Visual Studio 15 2017 Win64" .` for Visual Studio 2017 Professional

Build with \
`cmake --build . --target ALL_BUILD --config Release` or\
`cmake --build . --target ALL_BUILD --config Debug`

Required manual fixes
---------------------
For the Debug configurations:\
Under Project Properties->Linker->Input remove all non debug wt libs (e.g. wt.lib, debug version is wtd.lib)