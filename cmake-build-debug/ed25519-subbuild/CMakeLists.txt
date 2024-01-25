# Distributed under the OSI-approved BSD 3-Clause License.  See accompanying
# file Copyright.txt or https://cmake.org/licensing for details.

cmake_minimum_required(VERSION 3.23.2)

# We name the project and the target for the ExternalProject_Add() call
# to something that will highlight to the user what we are working on if
# something goes wrong and an error message is produced.

project(ed25519-populate NONE)



include(ExternalProject)
ExternalProject_Add(ed25519-populate
                     "URL" "/Users/mcenk/Documents/Projects/rippled-cofactored-patch/rippled/src/ed25519-donna.orig" "PATCH_COMMAND" "/Applications/CLion.app/Contents/bin/cmake/mac/bin/cmake" "-E" "chdir" "../.." "git" "apply" "-p1" "/Users/mcenk/Documents/Projects/rippled-cofactored-patch/rippled/src/ed25519-donna.patch"
                    SOURCE_DIR          "/Users/mcenk/Documents/Projects/rippled-cofactored-patch/rippled/src/ed25519-donna"
                    BINARY_DIR          "/Users/mcenk/Documents/Projects/rippled-cofactored-patch/rippled/cmake-build-debug/ed25519-build"
                    CONFIGURE_COMMAND   ""
                    BUILD_COMMAND       ""
                    INSTALL_COMMAND     ""
                    TEST_COMMAND        ""
                    USES_TERMINAL_DOWNLOAD  YES
                    USES_TERMINAL_UPDATE    YES
                    USES_TERMINAL_PATCH     YES
)


