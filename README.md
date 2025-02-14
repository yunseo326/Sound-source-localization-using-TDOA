##this is Sound-source-localization-using-TDOA

##execute the code 
#1. install the library in the "requirement.txt"

#2. execute the code (if you have error in cmake then change the CMakeLists.txt)
```cpp
cd build
cmake ..
make
./main
```cpp

##execute the code 

```cpp
code flow
main -> process_audio (gcc_phat, fft -> caltegorize_value -> calculate_8_angles)  -> select_final_direction
```cpp

```cpp
final/src/_process_audio.cpp          : 
final/src/_gcc_phat.cpp               : calculate the TDOA 
final/src/_fft.cpp                    : calculate the TDOA 
final/src/_categorize_values.cpp      : calculate the quadrant using TDOA
final/src/_calculate_8_angles.cpp     : calculate the 4angle using quadrant
final/src/_select_final_direction.cpp : return mean of two angle making minimum difference between them.
```cpp