# Pandoc styles 

A set of styles I use for my work, using pandoc. Two examples, one for my employer 
[AbacusBio](https://abacusbio.com) and one for a project I work on [Genomics Aotearoa](https://genomics-aotearoa.org.nz)


## Clone

```
cd ~/git/ # if thats where you store git repos, if not make sure to modify 
git clone --recurse-submodules https://github.com/jduckles/pandoc_styles/
```

## Requirements

```
# Mac 
brew install pandoc 
# Linux (Ubuntu/Debian)
apt-get install pandoc
```

** Codimd CLI ** Details at: https://github.com/codimd/cli (requires curl, wget and jq to be installed)

## To create your own style

```
# In a clone of this repo 
mkdir <stylename>
cd <stlyename>
pandoc --print-default-data-file reference.docx > reference.docx
# Open reference.docx in Word, or Libre Office, make changes to the style settings, but don't change the document content.
#   Save reference.docx
# run n2d as:
cd ..
./n2d ############### outfile.docx <stylename>
```

You should be able to `mv n2d ~/bin/` (provided you have a ~/bin directory already) to make this runable from anywhere on your machine.
You may have to add `${HOME}/bin` to your `PATH` if it isn't there already. 

