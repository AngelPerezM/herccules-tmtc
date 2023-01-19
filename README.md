# TMTC Interface

Telemetry & Telecommand Interface (TMTC I/F) for the GSSW and OBSW communication of the HERCCULES system.

# Introduction

The TMTC I/F is defined by:
   1. A set of data types used to communicate the GSSW and OBSW.

   2. A set of rules for the encoding and decoding of the data types defined in *1.*.

   3. A set of function prototypes (the I/F) that must be implemented by the OBSW and GSSW.

The `Data_Types` directory contains the definition of these data types which are located in the `src` folder and written in the Abstract Syntax Notation 1 (ASN.1) description language.

The the [ASN1SCC](https://github.com/ttsiodras/asn1scc) compiler is used to automatically transform these data types into *(1)* C type declarations and *(2)*  a set of serialization and deserialization functions for each data type. These assets are located inside the `Data_Types/build/asn1sccGenerated/c` directory.

# How to set-up?

The `Data_Types` module is a Qt project
that makes use of the N7Space ASN1 editor.
The project was developed inside the TASTE Virtual Machine and *must* be opened with the `spacecreator.AppImange` command, rather that the useal `qtcreator`.