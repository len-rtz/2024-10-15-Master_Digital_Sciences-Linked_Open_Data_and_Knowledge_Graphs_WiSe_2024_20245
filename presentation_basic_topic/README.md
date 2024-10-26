# Basic presentation 

```
pandoc Example_presentation.md -t beamer -V aspectratio=169 -V theme:metropolis -o Example_presentation.pdf
```

should generate the PDF file `Example_presentation.pdf`.

```
pandoc Example_presentation.md -t beamer -V aspectratio=169 -V theme:metropolis -o Example_presentation.html
```

should generate the PDF file `Example_presentation.html`.

Please name your file accordingly e.g. "RDF.md" and in case you use
images with the same prefix e.g. `RDF_my_awesome_image_1.png`and place
them in the folder `ìmages`.
