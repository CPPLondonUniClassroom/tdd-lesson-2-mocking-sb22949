cmake_minimum_required(VERSION 3.11)
project(Blockbuster)

set(CMAKE_CXX_STANDARD 17)

add_executable(Blockbuster main.cpp
                include/interface/IRentable.h
                include/Video.h src/Video.cpp
                include/interface/ICustomer.h
                include/Money.h
                include/Customer.h
                src/Customer.cpp)
target_include_directories(Blockbuster PRIVATE include)

add_executable(TestBlockbuster test/testmain.cpp
                test/catch.hpp
                test/trompeloeil.hpp
                test/TestCustomer.cpp
                src/Customer.cpp include/Customer.h)
target_include_directories(TestBlockbuster PRIVATE include)