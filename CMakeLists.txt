cmake_minimum_required(VERSION 3.1.0 FATAL_ERROR)
project(DwarfTherapistManual)

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake/Modules")

include(UseLATEX)
add_latex_document("Dwarf Therapist.tex"
		   IMAGE_DIRS images
		   FORCE_PDF)

if(UNIX AND NOT APPLE)
	if(NOT DEFINED LATEX_OUTPUT_PATH)
		set(LATEX_OUTPUT_PATH ${CMAKE_CURRENT_BINARY_DIR})
	endif()
	# Installation is currently Linux-only
	install(FILES "${LATEX_OUTPUT_PATH}/Dwarf Therapist.pdf"
		DESTINATION share/doc/dwarftherapist)
endif()
