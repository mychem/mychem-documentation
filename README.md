# Mychem Documentation
The Mychem documentation is based on DocBook. The last version is available online at [Mychem documentation](https://sourceforge.net/projects/mychem/files/documentation/). You can also generate yourself the PDF or HTML version of the documentation with the following instructions.

## PDF
    xsltproc \
    --stringparam use.extensions 0 \
    --stringparam paper.type A4 \
    --stringparam page.orientation portrait \
    --stringparam page.margin.inner 0.4in \
    --stringparam page.margin.outer 0.4in \
    --stringparam section.autolabel 1 \
    --stringparam section.label.includes.component.label 1 \
    --stringparam fop1.extensions 1 \
    --output mychem.fo \
    /usr/share/xml/docbook/stylesheet/nwalsh/fo/docbook.xsl mychem.xml
    fop -fo mychem.fo -pdf mychem.pdf

## HTML
    xsltproc \
    --stringparam use.extensions 0 \
    --stringparam paper.type A4 \
    --stringparam page.orientation portrait \
    --stringparam page.margin.inner 0.4in \
    --stringparam page.margin.outer 0.4in \
    --stringparam section.autolabel 1 \
    --stringparam section.label.includes.component.label 1 \
    --stringparam fop1.extensions 1 \
    --output mychem.fo \
    /usr/share/xml/docbook/stylesheet/nwalsh/xhtml/docbook.xsl mychem.pdf
