#   ************    LibreSilicon's DanubeRiver      *******************
#
#   Organisation:   Chipforge
#                   Germany / European Union
#
#   Profile:        Chipforge focus on fine System-on-Chip Cores in
#                   Verilog HDL Code which are easy understandable and
#                   adjustable. For further information see
#                           www.chipforge.org
#                   there are projects from small cores up to PCBs, too.
#
#   File:           DanubeRiver/GNUmakefile
#
#   Purpose:        Root Makefile
#
#   ************    GNU Make 3.80 Source Code       ****************
#
#   ////////////////////////////////////////////////////////////////
#
#   Copyright (c) 2021 by
#                   chipforge <stdcelllib@nospam.chipforge.org>
#   All rights reserved.
#
#       This Standard Cell Library is licensed under the Libre Silicon
#       public license; you can redistribute it and/or modify it under
#       the terms of the Libre Silicon public license as published by
#       the Libre Silicon alliance, either version 1 of the License, or
#       (at your option) any later version.
#
#       This design is distributed in the hope that it will be useful,
#       but WITHOUT ANY WARRANTY; without even the implied warranty of
#       MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.
#       See the Libre Silicon Public License for more details.
#
#   ////////////////////////////////////////////////////////////////////

#   project root directory, relative, used inside include.mk file
PRD =               .

#   common definitions

include $(PRD)/include.mk

DISTRIBUTION =  $(DOCUMENTSDIR)/*.pdf \
                # still incomplete

#   ----------------------------------------------------------------
#               DEFAULT TARGETS
#   ----------------------------------------------------------------

#   display help screen if no target is specified

.PHONY: help
help:
	#   ----------------------------------------------------------
	#       available targets:
	#   ----------------------------------------------------------
	#
	#   help       - print this help screen
	#   dist       - build a tarball with all important files
	#   clean      - clean up all intermediate files
	#
	#   layout     - generate physical layouts
	#   doc        - generate complete documentation
	#

#   'clean' directories

.PHONY: clean
clean:
	$(MAKE) -C $(DOCUMENTSDIR) $@

#   ----------------------------------------------------------------
#               LAYOUT TARGETS
#   ----------------------------------------------------------------

#   generate layout for all known cells

.PHONY: layout
layout:
	$(MAKE) -C $(LAYOUTDIR) $@

#   ----------------------------------------------------------------
#               DOCUMENTATION TARGETS
#   ----------------------------------------------------------------

.PHONY: doc
doc:
	$(MAKE) -C $(DOCUMENTSDIR) $@

#   ----------------------------------------------------------------
#               DISTRIBUTION
#   ----------------------------------------------------------------

#   make archive by building a tarball with all important files

.PHONY: dist
dist: clean doc
	$(TAR) -cvf $(PROJECT)_$(DATE).tgz $(DISTRIBUTION)

