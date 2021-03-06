# Debugging Information Testing

This is a python reimplementation for the debug-information testing framework for the paper 

- Debug Information Validation for Optimized Code in *PLDI* 2020 by Yuanbo Li, Shuo Ding, Qirun Zhang, Davide Italiano

## Dependency:
    
This project depends on the following tools, please make sure you have the following tools available:
        
- [csmith](https://embed.cs.utah.edu/csmith/) 
- [compcert](http://compcert.inria.fr/)
- [gcovr](https://gcovr.com/en/stable/)
- [gcc](https://gcc.gnu.org/)
- [clang](https://clang.llvm.org/)
- [dexter](https://github.com/llvm/llvm-project/tree/master/debuginfo-tests/dexter) (code included in the repo)

### Remark
Please use the dexter in our repository, if you have other versions of dexter installed. The code of dexter in our repo has been slightly modified.

To test a clang compiler, please set "clang" as a softlink to the clang compiler with the desired version you wish to test.

## Usage:
First config the compiler and flag options for the debug-information testing and set the options in config.txt
```
config.txt:
testing compiler: clang
testing compiler flags: -O2 -g
```

Then run the config.sh before the actual use of the testing framework.
```
    ./config.sh
    python3 test-debug-info.py
```
Bugs found by the framework will be put under "bugs" directory.
