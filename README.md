# LibTooling-and-LibASTMatchers

This source code is intended to show how to build a useful source-to-source translation tool based on Clang’s LibTooling. It is explicitly aimed at people who are new to Clang, so all you should need is a working knowledge of C++ and the command line.

In order to work on the compiler, you need some basic knowledge of the abstract syntax tree (AST). To this end, the reader is encouraged to skim the Introduction to the Clang AST

Step 0: Obtaining Clang
-----------------
As Clang is part of the LLVM project, you’ll need to download LLVM’s source code first. Both Clang and LLVM are in the same git repository, under different directorie
-  `mkdir ~/clang-llvm && cd ~/clang-llvm`
-  `git clone https://github.com/llvm/llvm-project.git`

Next you need to obtain the CMake build system and Ninja build tool.
-  `cd ~/clang-llvm`
-  `git clone https://github.com/martine/ninja.git`
-  `cd ninja`
-  `git checkout release`
-  `./configure.py --bootstrap`
-  `sudo cp ninja /usr/bin/`
-  `cd ~/clang-llvm`
-  `git clone https://gitlab.kitware.com/cmake/cmake.git`
-  `cd cmake`
-  `git checkout next`
-  `./bootstrap`
-  `make`
-  `sudo make install`

Oay. Now we’ll build Clang!
- `sudo cp ninja /usr/bin/`
- `mkdir build && cd build`
- `cmake -G Ninja ../llvm-project/llvm -DLLVM_ENABLE_PROJECTS="clang;clang-tools-extra" -DCMAKE_BUILD_TYPE=Release -DLLVM_BUILD_TESTS=ON`
- `ninja`
- `ninja check`
- `ninja clang-test`
- `ninja install`

  
Installation:
-----------------
