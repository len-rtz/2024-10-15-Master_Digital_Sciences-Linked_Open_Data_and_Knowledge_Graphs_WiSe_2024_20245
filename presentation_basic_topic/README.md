# Basic presentation 

```
pandoc Example_presenation.md -t beamer -V aspectratio=169 -V theme:metropolis -o Example_presenation.pdf
```

should generate the PDF file `Example_presenation.pdf`.

```
pandoc Example_presenation.md -t beamer -V aspectratio=169 -V theme:metropolis -o Example_presenation.html
```

should generate the PDF file `Example_presenation.html`.

Please name your file accordingly e.g. "RDF.md" and in case you use
images with the same prefix e.g. `RDF_my_awesome_image_1.png`and place
them in the folder `ìmages`.
