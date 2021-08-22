PREFIX	?= /usr
DOCDIR	?= $(PREFIX)/share/doc/pam_python

.PHONY: build
build:	html/pam_python.html html/index.html

html/pam_python.html:
	sphinx-build -b html -E . html

html/index.html:
	ln -s pam_python.html html/index.html

.PHONY: install install-doc
install: install-doc
install-doc:
	mkdir -p $(DESTDIR)$(DOCDIR)/html
	cp -a html/* $(DESTDIR)$(DOCDIR)/html
	mkdir -p $(DESTDIR)$(DOCDIR)/examples
	cp -a ../examples $(DESTDIR)$(DOCDIR)/.

clean:
	rm -rf html
