# PDF Text Extraction Benchmark
This benachmark is about reading pure PDF files - notscanned documents and not documents that applied OCR.

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
|         Borb | 2022-06-04        |                 AGPL/Commercial |   2.0.27 |                                                           |
|    pypdfium2 | 2022-06-09        |      Apache-2.0 or BSD-3-Clause |    2.0.0 | PDFium (Foxit/Google)                                     |
| pdfminer.six | 2022-05-24        |                           MIT/X | 20220524 |                                                           |
|   pdfplumber | 2022-05-31        |                             MIT |    0.7.1 |                                                           |
|    pdftotext | -                 |                             GPL |   0.86.1 | build-essential libpoppler-cpp-dev pkg-config python3-dev |
|      PyMuPDF | 2022-06-27        | GNU AFFERO GPL 3.0 / Commerical |   1.20.0 | MuPDF                                                     |
|       PyPDF2 | 2022-06-30        |                    BSD 3-Clause |    2.4.1 |                                                           |
|         Tika | 2020-03-21        |                       Apache v2 |     1.24 | Apache Tika                                               |


## Text Extraction Speed

| #  |                          Library                          | Average | [   1   ](https://arxiv.org/pdf/2201.00214.pdf) | [   2   ](https://github.com/py-pdf/sample-files/raw/main/009-pdflatex-geotopo/GeoTopo.pdf) | [   3   ](https://arxiv.org/pdf/2201.00151.pdf) | [   4   ](https://arxiv.org/pdf/1707.09725.pdf) | [   5   ](https://arxiv.org/pdf/2201.00021.pdf) | [   6   ](https://arxiv.org/pdf/2201.00037.pdf) | [   7   ](https://arxiv.org/pdf/2201.00069.pdf) | [   8   ](https://arxiv.org/pdf/2201.00178.pdf) | [   9   ](https://arxiv.org/pdf/2201.00201.pdf) | [  10   ](https://arxiv.org/pdf/1602.06541.pdf) | [  11   ](https://arxiv.org/pdf/2201.00200.pdf) | [  12   ](https://arxiv.org/pdf/2201.00022.pdf) | [  13   ](https://arxiv.org/pdf/2201.00029.pdf) | [  14   ](https://arxiv.org/pdf/1601.03642.pdf) |
| :- | :-------------------------------------------------------- | :------ | :---------------------------------------------- | :------------------------------------------------------------------------------------------ | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- |
| 1  | [PyMuPDF        ](https://pypi.org/project/PyMuPDF/)      |    0.1s | 0.4s                                            | 0.3s                                                                                        | 0.2s                                            | 0.2s                                            | 0.1s                                            | 0.1s                                            | 0.0s                                            | 0.1s                                            | 0.0s                                            | 0.0s                                            | 0.0s                                            | 0.0s                                            | 0.0s                                            | 0.0s                                            |
| 2  | [pypdfium2      ](https://pypi.org/project/pypdfium2/)    |    0.2s | 0.5s                                            | 0.6s                                                                                        | 0.2s                                            | 0.5s                                            | 0.1s                                            | 0.2s                                            | 0.1s                                            | 0.1s                                            | 0.0s                                            | 0.1s                                            | 0.0s                                            | 0.1s                                            | 0.0s                                            | 0.0s                                            |
| 3  | [Tika           ](https://pypi.org/project/tika/)         |    0.2s | 1.0s                                            | 0.5s                                                                                        | 0.4s                                            | 0.4s                                            | 0.1s                                            | 0.2s                                            | 0.1s                                            | 0.1s                                            | 0.1s                                            | 0.1s                                            | 0.1s                                            | 0.1s                                            | 0.1s                                            | 0.0s                                            |
| 4  | [pdftotext      ](https://poppler.freedesktop.org/)       |    0.3s | 0.7s                                            | 0.9s                                                                                        | 0.3s                                            | 0.8s                                            | 0.1s                                            | 0.3s                                            | 0.2s                                            | 0.1s                                            | 0.0s                                            | 0.1s                                            | 0.1s                                            | 0.1s                                            | 0.0s                                            | 0.0s                                            |
| 5  | [PyPDF2         ](https://pypi.org/project/PyPDF2/)       |    2.3s | 17.3s                                           | 4.0s                                                                                        | 5.2s                                            | 2.0s                                            | 0.4s                                            | 0.7s                                            | 0.3s                                            | 0.3s                                            | 0.3s                                            | 0.4s                                            | 0.4s                                            | 0.2s                                            | 0.3s                                            | 0.1s                                            |
| 6  | [pdfminer.six   ](https://pypi.org/project/pdfminer.six/) |    7.1s | 41.7s                                           | 20.8s                                                                                       | 10.9s                                           | 8.4s                                            | 1.7s                                            | 3.5s                                            | 1.3s                                            | 2.1s                                            | 1.5s                                            | 2.0s                                            | 1.6s                                            | 1.6s                                            | 1.2s                                            | 0.7s                                            |
| 7  | [pdfplumber     ](https://pypi.org/project/pdfplumber/)   |    7.9s | 53.7s                                           | 13.5s                                                                                       | 14.1s                                           | 8.0s                                            | 2.7s                                            | 4.2s                                            | 2.3s                                            | 1.8s                                            | 1.6s                                            | 3.0s                                            | 1.9s                                            | 1.6s                                            | 1.1s                                            | 1.1s                                            |
| 8  | [Borb           ](https://pypi.org/project/borb/)         |   63.2s | 208.5s                                          | 301.5s                                                                                      | 2.8s                                            | 108.9s                                          | 26.5s                                           | 30.1s                                           | 95.8s                                           | 28.0s                                           | 23.5s                                           | 11.4s                                           | 8.9s                                            | 28.6s                                           | 6.4s                                            | 3.8s                                            |


## Watermarking Speed

| #  |                       Library                       | Average | [   1   ](https://arxiv.org/pdf/2201.00214.pdf) | [   2   ](https://github.com/py-pdf/sample-files/raw/main/009-pdflatex-geotopo/GeoTopo.pdf) | [   3   ](https://arxiv.org/pdf/2201.00151.pdf) | [   4   ](https://arxiv.org/pdf/1707.09725.pdf) | [   5   ](https://arxiv.org/pdf/2201.00021.pdf) | [   6   ](https://arxiv.org/pdf/2201.00037.pdf) | [   7   ](https://arxiv.org/pdf/2201.00069.pdf) | [   8   ](https://arxiv.org/pdf/2201.00178.pdf) | [   9   ](https://arxiv.org/pdf/2201.00201.pdf) | [  10   ](https://arxiv.org/pdf/1602.06541.pdf) | [  11   ](https://arxiv.org/pdf/2201.00200.pdf) | [  12   ](https://arxiv.org/pdf/2201.00022.pdf) | [  13   ](https://arxiv.org/pdf/2201.00029.pdf) | [  14   ](https://arxiv.org/pdf/1601.03642.pdf) |
| :- | :-------------------------------------------------- | :------ | :---------------------------------------------- | :------------------------------------------------------------------------------------------ | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- |
| 1  | [PyPDF2         ](https://pypi.org/project/PyPDF2/) |    5.9s | 17.3s                                           | 4.0s                                                                                        | 5.2s                                            | 2.0s                                            | 0.4s                                            | 0.7s                                            | 0.3s                                            | 0.3s                                            | 0.3s                                            | 0.4s                                            | 0.4s                                            | 0.2s                                            | 0.3s                                            | 0.1s                                            |

## Text Extraction Quality

| #  |                          Library                          | Average | [   1   ](https://arxiv.org/pdf/2201.00214.pdf) | [   2   ](https://github.com/py-pdf/sample-files/raw/main/009-pdflatex-geotopo/GeoTopo.pdf) | [   3   ](https://arxiv.org/pdf/2201.00151.pdf) | [   4   ](https://arxiv.org/pdf/1707.09725.pdf) | [   5   ](https://arxiv.org/pdf/2201.00021.pdf) | [   6   ](https://arxiv.org/pdf/2201.00037.pdf) | [   7   ](https://arxiv.org/pdf/2201.00069.pdf) | [   8   ](https://arxiv.org/pdf/2201.00178.pdf) | [   9   ](https://arxiv.org/pdf/2201.00201.pdf) | [  10   ](https://arxiv.org/pdf/1602.06541.pdf) | [  11   ](https://arxiv.org/pdf/2201.00200.pdf) | [  12   ](https://arxiv.org/pdf/2201.00022.pdf) | [  13   ](https://arxiv.org/pdf/2201.00029.pdf) | [  14   ](https://arxiv.org/pdf/1601.03642.pdf) |
| :- | :-------------------------------------------------------- | :------ | :---------------------------------------------- | :------------------------------------------------------------------------------------------ | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- | :---------------------------------------------- |
| 1  | [pypdfium2      ](https://pypi.org/project/pypdfium2/)    |  98%    |  99%                                            |  97%                                                                                        |  95%                                            |  97%                                            |  98%                                            |  96%                                            |  99%                                            |  96%                                            |  99%                                            |  99%                                            |  98%                                            |  98%                                            |  99%                                            |  99%                                            |
| 2  | [PyMuPDF        ](https://pypi.org/project/PyMuPDF/)      |  97%    |  98%                                            |  97%                                                                                        |  94%                                            |  95%                                            |  98%                                            |  96%                                            |  99%                                            |  95%                                            |  99%                                            |  98%                                            |  98%                                            |  98%                                            |  98%                                            |  99%                                            |
| 3  | [Tika           ](https://pypi.org/project/tika/)         |  97%    |  99%                                            |  99%                                                                                        |  94%                                            |  99%                                            |  98%                                            |  97%                                            |  94%                                            |  99%                                            |  99%                                            |  93%                                            |  98%                                            |  94%                                            |  98%                                            |  96%                                            |
| 4  | [PyPDF2         ](https://pypi.org/project/PyPDF2/)       |  96%    |  97%                                            |  87%                                                                                        |  93%                                            |  94%                                            |  97%                                            |  94%                                            |  96%                                            |  93%                                            |  98%                                            |  98%                                            |  97%                                            |  97%                                            |  98%                                            |  99%                                            |
| 5  | [pdftotext      ](https://poppler.freedesktop.org/)       |  93%    |  96%                                            |  93%                                                                                        |  91%                                            |  92%                                            |  92%                                            |  96%                                            |  96%                                            |  94%                                            |  97%                                            |  83%                                            |  94%                                            |  97%                                            |  97%                                            |  79%                                            |
| 6  | [pdfminer.six   ](https://pypi.org/project/pdfminer.six/) |  90%    |  95%                                            |  79%                                                                                        |  87%                                            |  90%                                            |  86%                                            |  94%                                            |  96%                                            |  91%                                            |  92%                                            |  92%                                            |  94%                                            |  86%                                            |  98%                                            |  86%                                            |
| 7  | [pdfplumber     ](https://pypi.org/project/pdfplumber/)   |  74%    |  93%                                            |  84%                                                                                        |  61%                                            |  94%                                            |  61%                                            |  93%                                            |  61%                                            |  86%                                            |  57%                                            |  59%                                            |  67%                                            |  59%                                            |  97%                                            |  67%                                            |
| 8  | [Borb           ](https://pypi.org/project/borb/)         |  53%    |  72%                                            |  86%                                                                                        |   0%                                            |  40%                                            |  67%                                            |  94%                                            |   0%                                            |  62%                                            |  69%                                            |  56%                                            |  75%                                            |  52%                                            |   0%                                            |  64%                                            |
