# PDF Flatten
Linux script to flatten mark-ups added to .pdf files by editors such as Okular, LibreOffice Draw or Adobe Acrobat via Nautilus or other file managers.

If you are trying to redact sections of a .pdf document many of the editors simply highlight in black or draw a black text box over the text in question.  Often trying to highlight the area in question will reveal your supposedly / intended redacted text.  This script flattens the various layers into a single-layer document so that the redacted text cannot be revealed.
# Installation
This is a single bash script, which you should copy to the ~/.local/share/nautilus/scripts/ folder.

For Caja (the file manager used in Ubuntu Mate, etc.) the script directory is the ~/.config/caja/scripts/ folder.  Check your distros documentation for the appropriate script folder for your file manager, if different.

You need to set appropriate execution rights (via Properties > Permissions > Allow executing file as program or `chmod +x`). 

You must also ensure that you have Zenity installed. The script uses either pdf2ps (standard in Ubuntu or can be installed from Poppler Tools) or convert (from ImageMagick but standard in Ubuntu)
`sudo apt install zenity`
# Usage
Once installed, right clicking on a PDF file will show a "Scripts" menu, with a "Flatten Marked-Up PDF to Done" submenu entry.  If it does not already exist, the script will create a /Done folder.  The .pdf file will be flattened and will be saved in the /Done folder.  The original file will be preserved.
# Credits
Thanks to Ricardo Ferreira (https://launchpad.net/compress-pdf/) for the original work on Compress PDF which was the inspiration for this project.

Thanks to my work colleagues for their work on translating this project.  Ania Lala, Dr Maury Guerrero, Hariraj Ji, Dr Georgios Diakidis, Dr Paul Ayadoe, Dr Khalid Siddig, Dr Asim Nayeem.
