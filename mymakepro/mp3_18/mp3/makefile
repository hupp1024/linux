.PHONY:all

export BUILD_ROOT = $(shell pwd)
export HEAD_PATH = $(BUILD_ROOT)/inc
all:
	make -C lcd
	make -C usb
	make -C media
	make -C math
	make -C app
clean:
	rm -rf ./mp3 ./app/link_obj ./app/dep ./app/lib_obj ./lib

