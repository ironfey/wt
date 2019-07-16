CMAKE_MINIMUM_REQUIRED(VERSION 3.14)
Project(hello)

INCLUDE_DIRECTORIES(./Wt-4.0.5-msvs2017-Windows-x64-SDK/include)
LINK_DIRECTORIES(./Wt-4.0.5-msvs2017-Windows-x64-SDK/lib)


ADD_EXECUTABLE(hello.wt
  hello.cpp
)

# For FastCGI deployment:
#TARGET_LINK_LIBRARIES(myprog.wt
#  wtfcgi wt someotherlib
#)

#Or, for built-in httpd deployment:
TARGET_LINK_LIBRARIES(hello.wt
  optimized wthttp wt debug wthttpd
  optimized wt debug wtd
)
