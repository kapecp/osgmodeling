SET(EXAMPLE_NAME osgmodelingbasic)
SET(EXAMPLE_FILES
    osgmodelingbasic.cpp
)
ADD_EXECUTABLE(${EXAMPLE_NAME} ${EXAMPLE_FILES})
SET_TARGET_PROPERTIES(${EXAMPLE_NAME} PROPERTIES PROJECT_LABEL "${EXAMPLE_NAME}")
SET_TARGET_PROPERTIES(${EXAMPLE_NAME} PROPERTIES OUTPUT_NAME ${EXAMPLE_NAME})

TARGET_LINK_LIBRARIES(${EXAMPLE_NAME} osgModeling ${OPENSCENEGRAPH_LIBRARIES} )

INSTALL(TARGETS ${EXAMPLE_NAME} RUNTIME DESTINATION ${CMAKE_INSTALL_PREFIX}/bin)
