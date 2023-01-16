# Main Chocolate Engine Repo

- Clone this repo with --recursive
- Enter `chocolate/thirdparty` and run the `thirdparty.py` script to download and compile thirdparty stuff
- Run `cmake -B build .` on Windows, or `cmake -B build. -DCMAKE_BUILD_TYPE=Debug .` on Linux (also Release is an option)
- Finish with standard cmake build stuff (VS2022 on Windows, `make -j 8` on linux)
- Run `output/sidurylauncher.exe` to run the engine
