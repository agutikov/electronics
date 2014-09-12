
NAME=mpx2202_breakout

.PHONY: all pdf clean eps

all: ps
	
ps: bottom.ps	
	
bottom.ps: ${NAME}.pcb Makefile
	pcb -x ps --layer-stack "bottom" --media A4 --drill-copper --auto-mirror --psfile bottom.ps --monochrome $< 
	
png: ${NAME}.png	
	
${NAME}.png: ${NAME}.pcb Makefile
	pcb -x png --outfile ${NAME}.png --photo-mode --dpi 300 $<

clean:
	rm -f *.pdf *.out *.aux *.eps *.ps *.log *.png





