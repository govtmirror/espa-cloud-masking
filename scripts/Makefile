#-----------------------------------------------------------------------------
# Makefile
#
# Simple makefile for installing the scripts.
#-----------------------------------------------------------------------------
.PHONY: all install clean

# Inherit from upper-level make.config
TOP = ..
include $(TOP)/make.config

SCRIPTS = cloud_masking.py

#-----------------------------------------------------------------------------
all:

#-----------------------------------------------------------------------------
install:
	install -d $(link_path)
	install -d $(bin_install_path)
	@for script in $(SCRIPTS); do \
            cmd="install -m 755 $$script $(bin_install_path)"; \
            echo "$$cmd"; $$cmd; \
            cmd="ln -sf $(link_source_path)/$$script $(link_path)/$$script"; \
            echo "$$cmd"; $$cmd; \
        done;

#-----------------------------------------------------------------------------
clean:

