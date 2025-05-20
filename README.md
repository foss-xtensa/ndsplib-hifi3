# HiFi_3z_NDSP
* NatureDSP Library for HiFi3 & HiFi3z DSP cores
* The source code is common to both HiFi-3 and HiFi-3Z cores.
* The xws provided supports both HiFi3 and HiFi3z.  
* Select the required HiFi-3 or HiFi-3z core for building, in both xws and linux environments. 

# The repo is organized as follows.

## xws:
  * Last stable release version of the NDSP contains two xws files.
  * An xws each, for the library-kernels and the test-driver.
    Ex : HiFi3_VFPU_Library_v5_0_0.xws & HiFi3_VFPU_Demo_v5_0_0.xws
  * Building and executing the xws in Xtensa Xplorer is described in the API Reference Document. 
  * Building and executing the source code in linux is described in the https://github.com/foss-xtensa/ndsplib-hifi3z/tree/main/doc. 
  * Detailed release documentation can be extracted from lib.xws/doc folder.

### Release v5.0.0 Brief:
- This is the GitHub release package created with the GA release V5.0.0. 
* Release Date : May 2025.
* The source code has been updated to make it compatible with RJ-2024.4 tool chain.
* Verification & testing has been done with various HiFi-3 (LX6.0.2)and HiFi-3z cores (LX8.0.3), with RJ-2024.4 tool chain 
* Sanity testing has been done for backward compatibility on xt-clang using RJ-2024.3 tool chain (LX8.0.3) core for HiFi3z and LX6 cores for HiFI3..   

* Known issues: 
  - For dct functional regression in -func_brief and -func_full, the test vectors are picked up from the sanity folder.   
   
## NDSP_HiFi3z
* This contains the source code (NDSP_HiFi3_v500.zip) along with make files that will build in linux environment.  

## doc folder
This contains help documentation on how to build the source code in linux and run the performance and functional regressions. 
