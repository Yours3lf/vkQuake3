file(GLOB zlibSrc
	"*.h"
	"*.c"
)

add_library(zlib STATIC ${zlibSrc})
target_compile_options(zlib PRIVATE -Wall -Werror=implicit-function-declaration -std=c11 -march=${ARCH_STRING} -fPIC)
