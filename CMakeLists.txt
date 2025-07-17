cmake_minimum_required(VERSION 3.21)
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# iOS-specific architecture configuration
if ("${CMAKE_SYSTEM_NAME}" STREQUAL "iOS" OR IOS)
    set(CMAKE_OSX_ARCHITECTURES "arm64")
else()
    set(CMAKE_OSX_ARCHITECTURES "arm64;x86_64")
endif()

set(CMAKE_CXX_VISIBILITY_PRESET hidden)

project(xdBot2 VERSION 1.0.0)

add_library(${PROJECT_NAME} SHARED
    src/main.cpp
    src/global.cpp
    src/macro.cpp
    src/keybinds.cpp
    src/utils/utils.cpp
    src/gdr/gdr.cpp
    src/renderer/renderer.cpp
    src/hacks/other.cpp
    src/hacks/tps_bypass.cpp
    src/hacks/frame_stepper.cpp
    src/hacks/layout_mode.cpp
    src/hacks/show_trajectory.cpp
    src/hacks/coin_finder.cpp
    src/hacks/clickbot.cpp
    src/hacks/autoclicker.cpp
    src/ui/macro_editor.cpp
    src/ui/button_edit_layer.cpp
    src/ui/game_ui.cpp
    src/ui/record_layer.cpp
    src/ui/render_settings_layer.cpp
    src/ui/load_macro_layer.cpp
    src/ui/clickbot_layer.cpp
    src/ui/button_setting.cpp
    src/practice_fixes/input.cpp
    src/practice_fixes/player.cpp
    src/practice_fixes/play_layer.cpp
)

# iOS-specific compiler flags and settings
if ("${CMAKE_SYSTEM_NAME}" STREQUAL "iOS" OR IOS)
    target_compile_definitions(${PROJECT_NAME} PRIVATE GEODE_IS_IOS)
    
    # iOS-specific linker flags
    set_target_properties(${PROJECT_NAME} PROPERTIES
        XCODE_ATTRIBUTE_IPHONEOS_DEPLOYMENT_TARGET "14.0"
        XCODE_ATTRIBUTE_TARGETED_DEVICE_FAMILY "1,2"
    )
endif()

# Platform-specific source files
if (WIN32)
    target_sources(${PROJECT_NAME} PRIVATE
        # Windows-specific sources would go here if any
    )
elseif (ANDROID)
    target_sources(${PROJECT_NAME} PRIVATE
        # Android-specific sources would go here if any
    )
elseif ("${CMAKE_SYSTEM_NAME}" STREQUAL "iOS" OR IOS)
    target_sources(${PROJECT_NAME} PRIVATE
        # iOS-specific sources would go here if any
    )
endif()

if (NOT DEFINED ENV{GEODE_SDK})
    message(FATAL_ERROR "Unable to find Geode SDK! Please define GEODE_SDK environment variable to point to Geode")
else()
    message(STATUS "Found Geode: $ENV{GEODE_SDK}")
endif()

add_subdirectory($ENV{GEODE_SDK} ${CMAKE_CURRENT_BINARY_DIR}/geode)

setup_geode_mod(${PROJECT_NAME})
