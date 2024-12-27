# LibTooling-and-LibASTMatchers

This source code is intended to show how to build a useful source-to-source translation tool based on Clang’s LibTooling. It is explicitly aimed at people who are new to Clang, so all you should need is a working knowledge of C++ and the command line.

In order to work on the compiler, you need some basic knowledge of the abstract syntax tree (AST). To this end, the reader is encouraged to skim the Introduction to the Clang AST

Step 0: Obtaining Clang
-----------------
As Clang is part of the LLVM project, you’ll need to download LLVM’s source code first. Both Clang and LLVM are in the same git repository, under different directorie
-  `mkdir ~/clang-llvm && cd ~/clang-llvm`
-  `git clone https://github.com/llvm/llvm-project.git`
