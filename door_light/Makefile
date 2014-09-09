
NAME=door_light

.PHONY: all pdf clean eps

all: pdf

eps: bottom.eps

bottom.eps: ${NAME}.pcb
	pcb -x eps --layer-stack "bottom" --eps-file bottom.eps --monochrome --as-shown  $^  
	
png: ${NAME}.png	
	
${NAME}.png: ${NAME}.pcb
	pcb -x png --outfile ${NAME}.png --photo-mode --dpi 300 $^ 

pdf: template_eps.latex bottom.eps
	pdflatex $<

clean:
	rm -f *.pdf *.out *.aux *.eps *.ps *.log *.png





