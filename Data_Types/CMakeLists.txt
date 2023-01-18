##############################################
# Configuration for the HERCCULES Data types #
##############################################

cmake_minimum_required(VERSION 2.8)

project(Data_Types)

set(ASN1ACNSOURCES
    src/DataTypes.asn
    src/DataTypes.acn
    src/DataTypes-Telemetries.asn
    src/DataTypes-Telemetries.acn
    src/DataTypes-Telecommands.asn
    src/DataTypes-Telecommands.acn
    src/DataTypes-OperatingModes.asn
    src/DataTypes-OperatingModes.acn
    src/DataTypes-Subsystems.asn
    src/DataTypes-Subsystems.acn
    src/DataTypes-Events.asn
    src/DataTypes-Events.acn)

include(asn1sccSettings.cmake)
include(createFilesList.cmake)

set(SOURCES ${ASN1ACNSOURCES} ${ASN1SCC_PRODUCTS})

if(SOURCES)
    set(TARGET_NAME ${PROJECT_NAME})
    add_library(${TARGET_NAME} ${SOURCES})
endif()

include(configureAsn1SccTarget.cmake)
