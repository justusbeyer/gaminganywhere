
OS	= $(shell uname -s)
MACHINE	= $(shell uname -m)
OS_M	= $(OS).$(MACHINE)

#ifneq ($(OS_M),Linux.x86_64)
TARGET	= periodic event-posix
#else
#TARGET	= periodic
#endif

all:
	for t in $(TARGET); do make -C $$t || exit 1; done

install:
	for t in $(TARGET); do make -C $$t install || exit 1; done

clean:
	for t in $(TARGET); do make -C $$t clean || exit 1; done

