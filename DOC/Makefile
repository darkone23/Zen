############################################################################
#                                                                          #
#                The Zen Computational Linguistics Toolkit                 #
#                                                                          #
#                      Gérard Huet & Benoît Razet                          #
#                                                                          #
############################################################################
# Makefile of ZEN computational linguistics toolkit documentation          #
# V5.1 25-11-2018                                Copyright INRIA 2002-2018 #
############################################################################

#NOWEB=ocamlweb --old-fullpage -p "\usepackage{url} \usepackage{graphicx}"
NOWEB=ocamlweb -p "\usepackage{url} \usepackage{graphicx}"
OCAMLWEB=../../../ocamlweb-1.39/

TEX=intro.tex gen.tex list2.tex word.tex zipper.tex bintree.tex trie.tex lexicon.tex make_lex.tex share.tex mini.tex dagify.tex tertree.tex deco.tex lexmap.tex minimap.tex english.tex french.tex sanskrit.tex unglue.tex coroutines.tex biblio.tex supplements.tex zen.tex

DOC=zen.ps zen.pdf zen.html
ML=../ML

MAIN=$(ML)/pidgin.ml gen.tex $(ML)/gen.ml list2.tex $(ML)/list2.ml word.tex \
$(ML)/word.ml zipper.tex $(ML)/zipper.ml bintree.tex $(ML)/bintree.ml \
trie.tex $(ML)/trie.ml ascii.tex $(ML)/ascii.ml lexicon.tex $(ML)/lexicon.ml \
make_lex.tex $(ML)/make_lex.ml share.tex $(ML)/share.mli $(ML)/share.ml \
mini.tex $(ML)/mini.ml dagify.tex $(ML)/dagify.ml \
$(ML)/make_english_lexicon.ml english.tex $(ML)/zen_lexer.ml \
$(ML)/transducer.ml $(ML)/latin.ml french.tex $(ML)/make_french_lexicon.ml \
sanskrit.tex tertree.tex $(ML)/tertree.ml $(ML)/minitertree.ml deco.tex \
$(ML)/deco.ml lexmap.tex $(ML)/lexmap.ml minimap.tex $(ML)/minimap.mli \
$(ML)/minimap.ml unglue.tex $(ML)/unglue.ml $(ML)/unglue_test.ml \
coroutines.tex intro_aum0.tex $(ML)/aum0.mli react0.tex $(ML)/react0.ml \
aumt.tex $(ML)/aumt.mli reactt.tex $(ML)/reactt.ml regular.tex \
$(ML)/regular.ml linking.tex $(ML)/sanskrit_engine.ml conclusion.tex biblio.tex 

ZEN=intro.tex $(MAIN)

doc: tex # html 
 
tex: 
	$(NOWEB) --noweb $(ZEN) -o zen.tex
	pdflatex zen
#	dvips -Pwww -f zen.dvi > zen.ps
#	ps2pdf zen.ps

html: # fails because includegraphics
	$(NOWEB) --noweb --html --hevea-option "-I $(OCAMLWEB)" $(ZEN) -o zen.html



