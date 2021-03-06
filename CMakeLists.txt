cmake_minimum_required(VERSION 3.0.2 FATAL_ERROR)
project(LXQt)

message(STATUS "Building in SuperBuild mode. Builds all non optional LXQt CMake projects at\n once. Autotools/Automake based projects not yet supported.")
if (NOT DEFINED CMAKE_PREFIX_PATH AND NOT DEFINED ENV{CMAKE_PREFIX_PATH})
    message(FATAL_ERROR "CMAKE_PREFIX_PATH environment variable not set. When configuring for the first time, make sure CMAKE_PREFIX_PATH is set to the root of the build directory. It can be done by passing it to cmake as an command line parameter (e.g. cmake -DCMAKE_PREFIX_PATH=path_to_your_build_dir ..) OR by setting the CMAKE_PREFIX_PATH environment variable (e.g. export CMAKE_PREFIX_PATH=path_to_your_build_dir ..).")
endif()

add_subdirectory(lxqt-build-tools)
add_subdirectory(libqtxdg)
add_subdirectory(liblxqt)
add_subdirectory(libsysstat)
add_subdirectory(lxqt-session)
add_subdirectory(lxqt-qtplugin)
add_subdirectory(lxqt-globalkeys)
add_subdirectory(lxqt-notificationd)
add_subdirectory(lxqt-about)
add_subdirectory(lxqt-common)
add_subdirectory(lxqt-config)
add_subdirectory(lxqt-admin)
add_subdirectory(lxqt-openssh-askpass)
add_subdirectory(lxqt-panel)
add_subdirectory(lxqt-policykit)
add_subdirectory(lxqt-powermanagement)
add_subdirectory(lxqt-runner)
add_subdirectory(libfm-qt)
add_subdirectory(pcmanfm-qt)
add_subdirectory(lxqt-sudo)
add_subdirectory(pavucontrol-qt)
