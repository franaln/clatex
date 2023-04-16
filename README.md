clatex
======

- Compile latex using pdflatex/xelatex
- Simplified and coloured output
- Compile tikz/tables directly to pdf (without preamble and cropping output)
- Add plots/pdfs together in a single slide set
- Create slides templates
- Create and compile slides from python script (very useful for plots and use loops)
- Watch for file changes and recompile

To do:
- Improve documentation and examples


## Example of slides from python script

* slides.py:
```
bframe()
print('This is some text ...')
eframe()

bframe('Plots')
img(0.45, 'plot1.png')
img(0.45, 'plot2.png')
eframe()

for i in range(2):
    bframe(f'This is plot {i}')
    img(0.8, f'plot{i}.png')
    eframe()
```

* To compile
```
clatex slides.py
```
