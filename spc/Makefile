##################################################
# hse
##################################################

# WIZ ?= ../../../bin/wiz
# WIZ_INCLUDE ?= ../../../common
WIZ ?= wiz
WIZ_INCLUDE ?= $(HOME)/.local/include/wiz

TARGET := spc-core.bin
MAIN_PROG := main.wiz
DEPS := banks.wiz init.wiz
DEPS += Makefile

.PHONY: all clean

all: $(TARGET)

$(TARGET): $(MAIN_PROG) $(DEPS)
	$(WIZ) -I$(WIZ_INCLUDE)/spc --system=spc700 -o $@ $<


clean:
	rm -rf $(TARGET)
