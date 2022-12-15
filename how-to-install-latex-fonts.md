---
output: 
    pdf_document: 
        latex_engine: xelatex
---

# How to Install LaTeX fonts
1. Determine directory where LaTeX fonts are stored. In the case of an MacTeX, the directory is: `/usr/local/texlive/texmf-local`. If you use Linux or UNIX, type: `kpsewhich --var-value TEXMFLOCAL` in terminal. The result is the directory.
2. Download the font package ⁠- it usually is a zip file. Ideally download the font package that uses the TeX-Directory-Structure(TDS) as this guide will only work for fonts with this directory structure. Any other directory structure be fucked.
3. Unzip the font package and make **note of the names of each map file**. It will come in handy.Take the font package and move its subdirectories to the corresponding directories found in the LaTeX font directory.
4. On MacTeX, run: `sudo -H mktexlsr`  . For TeX Live, run: `mktexlsr` or `sudo -H mktexlsr`  .
5. For macOS, run: `sudo  -H  updmap-sys  --force  --enable  Map=nameOfMap.map`. For Linux or UNIX, run: `updmap-sys --force --enable Map=nameOfMap.map`.
6. Run step 4 to update database again. <br><br>


Step 4 updates the TeX file database.
Step 5 tells TeX about the new fonts.