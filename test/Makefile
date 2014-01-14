TEXINPUTS=../tex:
SRC=test000.tex test001.tex
#test001.tex
OBJ=${SRC:.tex=.pdf}
LOG=${SRC:.tex=.log}
AUX=${SRC:.tex=.aux}
OUT=${SRC:.tex=.out}
TMPS=${LOG} ${AUX} ${OUT}

all: ${OBJ}

clean:
	rm -f ${OBJ} ${TMPS}

%.pdf: %.tex
	while (TEXINPUTS=${TEXINPUTS} pdflatex $<; \
		grep "Rerun to get" $*.log;);\
	       do true;\
	done 

