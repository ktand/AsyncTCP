
if(ESP_PLATFORM)
    # using this library as a component in an ESP-IDF project
    idf_component_register(SRCS "src/AsyncTcp.cpp" INCLUDE_DIRS "src" REQUIRES "ArduinoCompatibility")
else()
    idf_component_register(SRCS "src/AsyncTcp.cpp" INCLUDE_DIRS "src" REQUIRES "arduino-esp32")
endif()


target_compile_options(${COMPONENT_TARGET} PRIVATE -fno-rtti)
