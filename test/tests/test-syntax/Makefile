.PHONY: test

MYVIM ?= nvim --headless

INMAKE := 1
export INMAKE

test: | syntax/asy.vim
	@$(MYVIM) -u test.vim

syntax/asy.vim:
	@echo -n "-- Fetching asy.vim ... "
	@mkdir -p syntax
	@wget \
	  https://raw.githubusercontent.com/vectorgraphics/asymptote/master/base/asy.vim \
	  -O syntax/asy.vim >/dev/null 2>&1
	@echo "done"
