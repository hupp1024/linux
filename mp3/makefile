.PHONY:all clean

SRCS = $(wildcard *.c)
OBJS = $(SRCS:.c=.o) 
DEPS = $(SRCS:.c=.d)
BIN = mp3
all:$(BIN) $(DEPS)
ifneq ("$(wildcard $(DEPS))","")
include $(DEPS)
endif
$(BIN):$(OBJS)
	gcc -o $@ $^
#usb.o:usb.c usb.h
%.o:%.c
	gcc -o $@ -c $(filter %.c,$^)
%.d:%.c
	gcc -MM $^ > $@
clean:
	rm -rf $(BIN) $(OBJS) $(DEPS)
