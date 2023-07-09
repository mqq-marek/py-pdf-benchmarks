# PDF Library Benchmarks
This benchmark is about reading pure PDF files - notscanned documents and not documents that applied OCR.

## Benchmarking machine
 Intel(R) Core(TM) i7-6700HQ CPU @ 2.60GHz

## Input Documents
| #  |                                               Name                                               | File Size | Pages |
| -: | :----------------------------------------------------------------------------------------------- | --------: | ----: |
|  1 | [2201.00214](https://arxiv.org/pdf/2201.00214.pdf)                                               |    2.4MiB |    22 |
|  2 | [GeoTopo-book](https://github.com/py-pdf/sample-files/raw/main/009-pdflatex-geotopo/GeoTopo.pdf) |    5.1MiB |   117 |
|  3 | [2201.00151](https://arxiv.org/pdf/2201.00151.pdf)                                               |    1.5MiB |    12 |
|  4 | [1707.09725](https://arxiv.org/pdf/1707.09725.pdf)                                               |    7.0MiB |   134 |
|  5 | [2201.00021](https://arxiv.org/pdf/2201.00021.pdf)                                               |    2.6MiB |    10 |
|  6 | [2201.00037](https://arxiv.org/pdf/2201.00037.pdf)                                               |    2.9MiB |    33 |
|  7 | [2201.00069](https://arxiv.org/pdf/2201.00069.pdf)                                               |   14.7MiB |    15 |
|  8 | [2201.00178](https://arxiv.org/pdf/2201.00178.pdf)                                               |    2.3MiB |    16 |
|  9 | [2201.00201](https://arxiv.org/pdf/2201.00201.pdf)                                               |    1.3MiB |     9 |
| 10 | [1602.06541](https://arxiv.org/pdf/1602.06541.pdf)                                               |    2.9MiB |    16 |
| 11 | [2201.00200](https://arxiv.org/pdf/2201.00200.pdf)                                               |  284.8KiB |     7 |
| 12 | [2201.00022](https://arxiv.org/pdf/2201.00022.pdf)                                               |    1.1MiB |    11 |
| 13 | [2201.00029](https://arxiv.org/pdf/2201.00029.pdf)                                               |  797.6KiB |    12 |
| 14 | [1601.03642](https://arxiv.org/pdf/1601.03642.pdf)                                               | 1004.9KiB |     8 |

## Libraries
|     Name     | Last PyPI Release |             License             | Version  |                       Dependencies                        |
| -----------: | :---------------- | ------------------------------: | -------: | :-------------------------------------------------------- |
|         Borb | 2023-06-23        |                 AGPL/Commercial |   2.1.15 |                                                           |
|    pypdfium2 | 2023-06-27        |      Apache-2.0 or BSD-3-Clause |   4.17.0 | PDFium (Foxit/Google)                                     |
| pdfminer.six | 2022-11-05        |                           MIT/X | 20221105 |                                                           |
|   pdfplumber | 2023-04-13        |                             MIT |    0.9.0 | pdfminer.six                                              |
|        pdfrw | 2017-09-18        |                             MIT |      0.4 |                                                           |
|    pdftotext | -                 |                             GPL |   0.86.1 | build-essential libpoppler-cpp-dev pkg-config python3-dev |
|      PyMuPDF | 2023-06-21        | GNU AFFERO GPL 3.0 / Commerical |   1.22.5 | MuPDF                                                     |
|        pypdf | 2023-07-09        |                    BSD 3-Clause |   3.12.1 |                                                           |
|         Tika | 2023-01-01        |                       Apache v2 |    2.6.0 | Apache Tika                                               |


## Text Extraction Speed

| #  |                          Library                          | Average | [   1   ](https://arxiv.org/pdf/2201.00214.pdf) | [   2   ](https://github.com/py-pdf/sample-files/raw/main/009-pdflatex-geotopo/GeoTopo.pdf) | [   3   ](https://arxiv.org/pdf/2201.00151.pdf) | [   4   ](https://arxiv.org/pdf/1707.09725.pdf) | [   5   ](https://arxiv.org/pdf/2201.00021.pdf) | [   6   ](https://arxiv.org/pdf/2201.00037.pdf) | [   7   ](https://arxiv.org/pdf/2201.00069.pdf) | [   8   ](https://arxiv.org/pdf/2201.00178.pdf) | [   9   ](https://arxiv.org/pdf/2201.00201.pdf) | [  10   ](https://arxiv.org/pdf/1602.06541.pdf) | [  11   ](https://arxiv.org/pdf/2201.00200.pdf) | [  12   ](https://arxiv.org/pdf/2201.00022.pdf) | [  13   ](https://arxiv.org/pdf/2201.00029.pdf) | [  14   ](https://arxiv.org/pdf/1601.03642.pdf) |
| :- | :-------------------------------------------------------- | :------ | :---------------------------------------------- | :------------------------------------------------------------------------------------------ | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- |
| 1  | [PyMuPDF        ](https://pypi.org/project/PyMuPDF/)      |    0.1s | 0.4s                                            | 0.3s                                                                                        | 0.2s                                            | 0.2s                                            | 0.0s                                            | 0.1s                                            | 0.0s                                            | 0.0s                                            | 0.0s                                            | 0.1s                                            | 0.0s                                            | 0.0s                                            | 0.0s                                            | 0.0s                                            |
| 2  | [pypdfium2      ](https://pypi.org/project/pypdfium2/)    |    0.1s | 0.5s                                            | 0.3s                                                                                        | 0.2s                                            | 0.2s                                            | 0.0s                                            | 0.1s                                            | 0.1s                                            | 0.0s                                            | 0.0s                                            | 0.1s                                            | 0.0s                                            | 0.0s                                            | 0.0s                                            | 0.0s                                            |
| 3  | [Tika           ](https://pypi.org/project/tika/)         |    0.2s | 1.1s                                            | 0.4s                                                                                        | 0.4s                                            | 0.4s                                            | 0.1s                                            | 0.1s                                            | 0.1s                                            | 0.1s                                            | 0.1s                                            | 0.1s                                            | 0.1s                                            | 0.1s                                            | 0.1s                                            | 0.1s                                            |
| 4  | [pdftotext      ](https://poppler.freedesktop.org/)       |    0.3s | 0.7s                                            | 0.9s                                                                                        | 0.3s                                            | 0.8s                                            | 0.1s                                            | 0.2s                                            | 0.2s                                            | 0.1s                                            | 0.0s                                            | 0.1s                                            | 0.1s                                            | 0.1s                                            | 0.0s                                            | 0.0s                                            |
| 5  | [pypdf          ](https://pypi.org/project/pypdf/)        |    2.2s | 16.3s                                           | 3.8s                                                                                        | 4.5s                                            | 1.7s                                            | 0.5s                                            | 0.8s                                            | 0.4s                                            | 0.4s                                            | 0.2s                                            | 0.5s                                            | 0.5s                                            | 0.3s                                            | 0.3s                                            | 0.1s                                            |
| 6  | [pdfminer.six   ](https://pypi.org/project/pdfminer.six/) |    4.7s | 26.2s                                           | 14.6s                                                                                       | 8.2s                                            | 5.4s                                            | 1.3s                                            | 2.1s                                            | 1.1s                                            | 1.2s                                            | 0.8s                                            | 1.7s                                            | 0.9s                                            | 0.9s                                            | 0.6s                                            | 0.5s                                            |
| 7  | [pdfplumber     ](https://pypi.org/project/pdfplumber/)   |    6.3s | 39.7s                                           | 10.7s                                                                                       | 11.6s                                           | 7.8s                                            | 2.1s                                            | 3.7s                                            | 1.9s                                            | 1.6s                                            | 1.6s                                            | 2.6s                                            | 1.7s                                            | 1.5s                                            | 1.0s                                            | 1.0s                                            |
| 8  | [Borb           ](https://pypi.org/project/borb/)         |   33.5s | 114.2s                                          | 101.7s                                                                                      | 1.3s                                            | 78.0s                                           | 20.5s                                           | 7.4s                                            | 80.2s                                           | 15.2s                                           | 17.6s                                           | 5.7s                                            | 3.6s                                            | 18.2s                                           | 3.3s                                            | 1.9s                                            |


## Image Extraction Speed

| #  |                          Library                          | Average | [   1   ](https://arxiv.org/pdf/2201.00214.pdf) | [   2   ](https://github.com/py-pdf/sample-files/raw/main/009-pdflatex-geotopo/GeoTopo.pdf) | [   3   ](https://arxiv.org/pdf/2201.00151.pdf) | [   4   ](https://arxiv.org/pdf/1707.09725.pdf) | [   5   ](https://arxiv.org/pdf/2201.00021.pdf) | [   6   ](https://arxiv.org/pdf/2201.00037.pdf) | [   7   ](https://arxiv.org/pdf/2201.00069.pdf) | [   8   ](https://arxiv.org/pdf/2201.00178.pdf) | [   9   ](https://arxiv.org/pdf/2201.00201.pdf) | [  10   ](https://arxiv.org/pdf/1602.06541.pdf) | [  11   ](https://arxiv.org/pdf/2201.00200.pdf) | [  12   ](https://arxiv.org/pdf/2201.00022.pdf) | [  13   ](https://arxiv.org/pdf/2201.00029.pdf) | [  14   ](https://arxiv.org/pdf/1601.03642.pdf) |
| :- | :-------------------------------------------------------- | :------ | :---------------------------------------------- | :------------------------------------------------------------------------------------------ | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- |
| 1  | [PyMuPDF        ](https://pypi.org/project/PyMuPDF/)      |    0.5s | 0.3s                                            | 0.5s                                                                                        | 0.0s                                            | 1.6s                                            | 0.4s                                            | 0.0s                                            | 2.8s                                            | 0.3s                                            | 0.4s                                            | 0.1s                                            | 0.0s                                            | 0.3s                                            | 0.2s                                            | 0.0s                                            |
| 2  | [pypdf          ](https://pypi.org/project/pypdf/)        |    3.7s | 18.0s                                           | 5.0s                                                                                        | 4.6s                                            | 12.3s                                           | 1.2s                                            | 0.4s                                            | 6.4s                                            | 1.1s                                            | 1.1s                                            | 0.6s                                            | 0.1s                                            | 0.8s                                            | 0.2s                                            | 0.1s                                            |
| 3  | [pdfminer.six   ](https://pypi.org/project/pdfminer.six/) |    6.8s | 31.8s                                           | 14.7s                                                                                       | 9.9s                                            | 26.5s                                           | 1.5s                                            | 2.3s                                            | 1.7s                                            | 1.3s                                            | 0.9s                                            | 1.6s                                            | 1.0s                                            | 1.1s                                            | 0.6s                                            | 0.5s                                            |


## Watermarking Speed

| #  |                       Library                        | Average | [   1   ](https://arxiv.org/pdf/2201.00214.pdf) | [   2   ](https://github.com/py-pdf/sample-files/raw/main/009-pdflatex-geotopo/GeoTopo.pdf) | [   3   ](https://arxiv.org/pdf/2201.00151.pdf) | [   4   ](https://arxiv.org/pdf/1707.09725.pdf) | [   5   ](https://arxiv.org/pdf/2201.00021.pdf) | [   6   ](https://arxiv.org/pdf/2201.00037.pdf) | [   7   ](https://arxiv.org/pdf/2201.00069.pdf) | [   8   ](https://arxiv.org/pdf/2201.00178.pdf) | [   9   ](https://arxiv.org/pdf/2201.00201.pdf) | [  10   ](https://arxiv.org/pdf/1602.06541.pdf) | [  11   ](https://arxiv.org/pdf/2201.00200.pdf) | [  12   ](https://arxiv.org/pdf/2201.00022.pdf) | [  13   ](https://arxiv.org/pdf/2201.00029.pdf) | [  14   ](https://arxiv.org/pdf/1601.03642.pdf) |
| :- | :--------------------------------------------------- | :------ | :---------------------------------------------- | :------------------------------------------------------------------------------------------ | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- |
| 1  | [PyMuPDF        ](https://pypi.org/project/PyMuPDF/) |    0.0s | 0.0s                                            | 0.1s                                                                                        | 0.0s                                            | 0.1s                                            | 0.0s                                            | 0.0s                                            | 0.0s                                            | 0.0s                                            | 0.0s                                            | 0.0s                                            | 0.0s                                            | 0.0s                                            | 0.0s                                            | 0.0s                                            |
| 2  | [pdfrw          ](https://pypi.org/project/pdfrw/)   |    0.1s | 0.0s                                            | 0.3s                                                                                        | 0.0s                                            | 0.3s                                            | 0.1s                                            | 0.1s                                            | 0.1s                                            | 0.1s                                            | 0.1s                                            | 0.1s                                            | 0.0s                                            | 0.1s                                            | 0.0s                                            | 0.0s                                            |
| 3  | [pypdf          ](https://pypi.org/project/pypdf/)   |   10.2s | 80.7s                                           | 17.9s                                                                                       | 23.8s                                           | 8.0s                                            | 1.2s                                            | 2.8s                                            | 1.4s                                            | 1.6s                                            | 1.0s                                            | 2.0s                                            | 0.8s                                            | 1.2s                                            | 0.2s                                            | 0.6s                                            |


## Watermarking File Size

| #  |                       Library                        | Average | [   1   ](https://arxiv.org/pdf/2201.00214.pdf) | [   2   ](https://github.com/py-pdf/sample-files/raw/main/009-pdflatex-geotopo/GeoTopo.pdf) | [   3   ](https://arxiv.org/pdf/2201.00151.pdf) | [   4   ](https://arxiv.org/pdf/1707.09725.pdf) | [   5   ](https://arxiv.org/pdf/2201.00021.pdf) | [   6   ](https://arxiv.org/pdf/2201.00037.pdf) | [   7   ](https://arxiv.org/pdf/2201.00069.pdf) | [   8   ](https://arxiv.org/pdf/2201.00178.pdf) | [   9   ](https://arxiv.org/pdf/2201.00201.pdf) | [  10   ](https://arxiv.org/pdf/1602.06541.pdf) | [  11   ](https://arxiv.org/pdf/2201.00200.pdf) | [  12   ](https://arxiv.org/pdf/2201.00022.pdf) | [  13   ](https://arxiv.org/pdf/2201.00029.pdf) | [  14   ](https://arxiv.org/pdf/1601.03642.pdf) |
| :- | :--------------------------------------------------- | :------ | :---------------------------------------------- | :------------------------------------------------------------------------------------------ | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- |
| 1  | [pdfrw          ](https://pypi.org/project/pdfrw/)   | 3.4MB   | 2.5MB                                           | 5.7MB                                                                                       | 1.6MB                                           | 7.3MB                                           | 2.7MB                                           | 3.1MB                                           | 15.4MB                                          | 2.4MB                                           | 1.3MB                                           | 3.0MB                                           | 0.3MB                                           | 1.1MB                                           | 0.8MB                                           | 1.0MB                                           |
| 2  | [pypdf          ](https://pypi.org/project/pypdf/)   | 3.5MB   | 2.8MB                                           | 5.8MB                                                                                       | 1.8MB                                           | 7.3MB                                           | 2.7MB                                           | 3.1MB                                           | 15.4MB                                          | 2.4MB                                           | 1.3MB                                           | 3.0MB                                           | 0.3MB                                           | 1.1MB                                           | 0.8MB                                           | 1.0MB                                           |
| 3  | [PyMuPDF        ](https://pypi.org/project/PyMuPDF/) | 3.7MB   | 2.7MB                                           | 6.8MB                                                                                       | 1.7MB                                           | 8.5MB                                           | 2.8MB                                           | 3.4MB                                           | 15.5MB                                          | 2.5MB                                           | 1.4MB                                           | 3.2MB                                           | 0.3MB                                           | 1.2MB                                           | 0.9MB                                           | 1.1MB                                           |

## Text Extraction Quality

| #  |                          Library                          | Average | [   1   ](https://arxiv.org/pdf/2201.00214.pdf) | [   2   ](https://github.com/py-pdf/sample-files/raw/main/009-pdflatex-geotopo/GeoTopo.pdf) | [   3   ](https://arxiv.org/pdf/2201.00151.pdf) | [   4   ](https://arxiv.org/pdf/1707.09725.pdf) | [   5   ](https://arxiv.org/pdf/2201.00021.pdf) | [   6   ](https://arxiv.org/pdf/2201.00037.pdf) | [   7   ](https://arxiv.org/pdf/2201.00069.pdf) | [   8   ](https://arxiv.org/pdf/2201.00178.pdf) | [   9   ](https://arxiv.org/pdf/2201.00201.pdf) | [  10   ](https://arxiv.org/pdf/1602.06541.pdf) | [  11   ](https://arxiv.org/pdf/2201.00200.pdf) | [  12   ](https://arxiv.org/pdf/2201.00022.pdf) | [  13   ](https://arxiv.org/pdf/2201.00029.pdf) | [  14   ](https://arxiv.org/pdf/1601.03642.pdf) |
| :- | :-------------------------------------------------------- | :------ | :---------------------------------------------- | :------------------------------------------------------------------------------------------ | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- |
| 1  | [pypdfium2      ](https://pypi.org/project/pypdfium2/)    |  98%    |  99%                                            |  97%                                                                                        |  95%                                            |  97%                                            |  98%                                            |  96%                                            |  99%                                            |  96%                                            |  99%                                            |  99%                                            |  98%                                            |  98%                                            |  99%                                            |  99%                                            |
| 2  | [PyMuPDF        ](https://pypi.org/project/PyMuPDF/)      |  97%    |  98%                                            |  97%                                                                                        |  94%                                            |  95%                                            |  98%                                            |  96%                                            |  99%                                            |  95%                                            |  99%                                            |  98%                                            |  98%                                            |  98%                                            |  98%                                            |  99%                                            |
| 3  | [Tika           ](https://pypi.org/project/tika/)         |  97%    |  99%                                            |  99%                                                                                        |  94%                                            |  99%                                            |  98%                                            |  97%                                            |  94%                                            |  99%                                            |  99%                                            |  93%                                            |  98%                                            |  94%                                            |  98%                                            |  96%                                            |
| 4  | [pypdf          ](https://pypi.org/project/pypdf/)        |  96%    |  98%                                            |  87%                                                                                        |  94%                                            |  94%                                            |  97%                                            |  94%                                            |  96%                                            |  93%                                            |  98%                                            |  98%                                            |  97%                                            |  97%                                            |  98%                                            |  99%                                            |
| 5  | [pdftotext      ](https://poppler.freedesktop.org/)       |  93%    |  96%                                            |  93%                                                                                        |  92%                                            |  92%                                            |  92%                                            |  96%                                            |  96%                                            |  94%                                            |  97%                                            |  83%                                            |  94%                                            |  97%                                            |  97%                                            |  79%                                            |
| 6  | [pdfminer.six   ](https://pypi.org/project/pdfminer.six/) |  90%    |  95%                                            |  79%                                                                                        |  87%                                            |  90%                                            |  86%                                            |  94%                                            |  96%                                            |  91%                                            |  92%                                            |  93%                                            |  94%                                            |  86%                                            |  98%                                            |  86%                                            |
| 7  | [pdfplumber     ](https://pypi.org/project/pdfplumber/)   |  75%    |  94%                                            |  84%                                                                                        |  61%                                            |  95%                                            |  61%                                            |  94%                                            |  62%                                            |  87%                                            |  57%                                            |  59%                                            |  67%                                            |  59%                                            |  99%                                            |  67%                                            |
| 8  | [Borb           ](https://pypi.org/project/borb/)         |  45%    |  70%                                            |  79%                                                                                        |   0%                                            |  39%                                            |  48%                                            |  92%                                            |   0%                                            |  63%                                            |  51%                                            |  41%                                            |  56%                                            |  43%                                            |   0%                                            |  53%                                            |
