# Arduino CMake configuration file to build TaskManager library

set(ARDUINO_DEFAULT_BOARD uno) # Default Board ID, when not specified
set(ARDUINO_DEFAULT_PORT com6) # Default Port, when not specified

generate_arduino_library(taskmanager_lib
    SRCS TaskManager.cpp
    HDRS TaskManager.h ClearInterrupt.h)

# Generate examples
generate_arduino_firmware(ledblinker
    SRCS examples/LedBlinker/LedBlinker.cpp
    HDRS examples/LedBlinker/LedBlinker.h
    LIBS taskmanager_lib)
