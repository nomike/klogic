cmake_minimum_required(VERSION 3.10)
project(KLogic)

find_package(ECM REQUIRED NO_MODULE)
set(CMAKE_MODULE_PATH ${ECM_MODULE_PATH})

set(CMAKE_AUTOMOC ON)

find_package(Qt5Widgets)
find_package(KF5 REQUIRED COMPONENTS
  CoreAddons
  WidgetsAddons
  DBusAddons
  KCMUtils
  KDELibs4Support)

add_definitions(-Wno-deprecated-declarations)

include(KDEInstallDirs)
include(KDECMakeSettings)
include(KDECompilerSettings NO_POLICY_SCOPE)
include(ECMOptionalAddSubdirectory)
include(FeatureSummary)
include_directories( ${KDE4_INCLUDES} ${QT_INCLUDES} )

#add_subdirectory( doc )
add_subdirectory( po )
add_subdirectory( src )
add_subdirectory( icons )
add_subdirectory( deviceIcons )


