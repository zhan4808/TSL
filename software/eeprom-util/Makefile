# POSIX build for EEPROM helper tools (macOS / Linux). MSVC users: open tsl-eeprom-utils.sln
CXX ?= c++
CXXFLAGS = -std=c++17 -Wall -Wextra -O2

BINDIR := bin
.PHONY: all clean

all: $(BINDIR)/tsl-make-block $(BINDIR)/tsl-read-block

$(BINDIR)/tsl-make-block: tsl-make-block/tsl-make-block.cpp tsl-make-block/pch.cpp tsl-make-block/pch.h | $(BINDIR)
	$(CXX) $(CXXFLAGS) -o $@ tsl-make-block/tsl-make-block.cpp tsl-make-block/pch.cpp

$(BINDIR)/tsl-read-block: tsl-read-block/tsl-read-block.cpp | $(BINDIR)
	$(CXX) $(CXXFLAGS) -o $@ $<

$(BINDIR):
	mkdir -p $(BINDIR)

clean:
	rm -rf $(BINDIR)
