add_executable(genrsakey src/genrsakey.cpp)
target_link_libraries(genrsakey PUBLIC Poco::Crypto Poco::Util Poco::XML)
if(MSVC)
	target_link_libraries(genrsakey PRIVATE OpenSSL::applink)
endif()
