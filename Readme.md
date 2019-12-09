# How to compile this project?

+ We will use the pandoc program for such task, it is pretty simple
1. First install it for your distro (note you may have to install latex/pdflatex separately, in arch it isnt pulled automatically...)
2. Go ahead and fill in something in the source file of your presentation, in markdown ,dont worry, it is easy(er. than latex...) and you can make it pretty with some of the beamer templates, it is also possible to download and apply user-made ones from the internet...
3. Time to compile!:  
```
pandoc source_file.md -t beamer -o pres.pdf
``` 
