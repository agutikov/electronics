
NAME=door_light

.PHONY: all pdf clean eps

all: pdf

eps: bottom.eps

bottom.eps: ${NAME}.pcb Makefile
	pcb -x eps --layer-stack "bottom" --eps-file bottom.eps --monochrome --eps-scale 1.05 --as-shown  $<  
	
ps: bottom.ps	
	
bottom.ps: ${NAME}.pcb Makefile
	pcb -x ps --layer-stack "bottom" --media A4 --drill-copper --auto-mirror --psfile bottom.ps --monochrome $< 
	
png: ${NAME}.png	
	
${NAME}.png: ${NAME}.pcb Makefile
	pcb -x png --outfile ${NAME}.png --photo-mode --dpi 300 $<

pdf: template_eps.latex bottom.eps
	pdflatex $<

clean:
	rm -f *.pdf *.out *.aux *.eps *.ps *.log *.png





