CC := gcc
CFLAGS := -g -Wall -Wextra
SRCS := $(wildcard */*.c)
BINS := $(patsubst %.c,build/%,$(SRCS))

.PHONY: all clean

all: $(BINS)

build/%: %.c 
	@mkdir -p $(dir $@)
	$(CC) $(CFLAGS) $< -o $@

clean:
	@rm -rf build 