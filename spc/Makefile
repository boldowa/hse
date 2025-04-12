##################################################
# hse
##################################################

# WIZ ?= ../../../bin/wiz
# WIZ_INCLUDE ?= ../../../common
WIZ ?= wiz
#WIZ_INCLUDE ?= $(HOME)/.local/include/wiz

TARGET := spc-core.bin
MAIN_PROG := main.wiz
DEPS := $(filter-out $(MAIN_PROG), $(wildcard *.wiz))
DEPS += Makefile

.PHONY: all clean

all: $(TARGET)

$(TARGET): $(MAIN_PROG) $(DEPS)
	$(WIZ) --system=spc700 -o $@ $<
#	$(WIZ) -I$(WIZ_INCLUDE)/spc --system=spc700 -o $@ $<


clean:
	rm -rf $(TARGET)
