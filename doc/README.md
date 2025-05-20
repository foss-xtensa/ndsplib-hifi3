# How to Build and Run the Source Code in Linux environment
  * Get the latest or required version of NDSP HiFi3/3z Code from GitHub archived in zip format.
  * This is a unified source code that compiles for both HiFi3 and HiFi3z cores.  
  * https://github.com/foss-xtensa/ndsplib-hifi3/tree/main/NDSP_HiFi3
  * Unzip or extract to the destination directory. 

## The source code is organized as follows.
  * **build** - contains the make file 
  * **library** - contains the optimized kernel functions for the HiFi core 
  * **testdriver** - contains the demo driver code to tun the library   

### It is assumed that the required HiFi core configurations and the Xtensa toolchain are installed in the Linux environment.
 An example .cshrc file  that sets up the build environment accordingly is provided for reference 

## Setting up the environment 
  * A typical way is to place this .cshrc file in your home directory and execute the following from the command line terminal... 
  * source ~/.cshrc 
  * rj4
  * setenv XTENSA_CORE CORE_NAME     
    Ex: setenv XTENSA_CORE AE_HiFi3_LE5_FP_XC
  

## Compiling the Source Code: 
  * Navigate to the testdriver directory:   …/NDSP_HiFi3z/build/project/xtclang/testdriver/
  * **CLEAN:**  make clean -j   
  * **BUILD:**  make all -j  


## Examples : Running the executable: 
  ### Navigate to the bin directory: …/NDSP_HiFi3z/build/bin
  ### Performance tests:
  * xt-run testdriver-AE_HiFi3_LE5_FP_XC__rj4__mm0_release_clang-Xtensa-release -mips -sanity         
  * xt-run testdriver-AE_HiFi3_LE5_FP_XC__rj4__mm0_release_clang-Xtensa-release -mips -brief 
  * xt-run testdriver-AE_HiFi3_LE5_FP_XC__rj4__mm0_release_clang-Xtensa-release -mips -full   
  ###	Functional tests:
  * xt-run --turbo testdriver-AE_HiFi3_LE5_FP_XC__rj4__mm0_release_clang-Xtensa-release -func -sanity
  * xt-run --turbo testdriver-AE_HiFi3_LE5_FP_XC__rj4__mm0_release_clang-Xtensa-release -func -brief
  * xt-run --turbo testdriver-AE_HiFi3_LE5_FP_XC__rj4__mm0_release_clang-Xtensa-release -func -full
  * xt-run --turbo testdriver-AE_HiFi3_LE5_FP_XC__rj4__mm0_release_clang-Xtensa-release -func -sanity -verbose 
  * xt-run --turbo testdriver-AE_HiFi3_LE5_FP_XC__rj4__mm0_release_clang-Xtensa-release -func -sanity -fir -verbose 
  * xt-run --turbo testdriver-AE_HiFi3_LE5_FP_XC__rj4__mm0_release_clang-Xtensa-release -func -brief -fir -iir -fft
