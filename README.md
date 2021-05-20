# RePlicator
Description:
RePlicator (Relative Plagiarism Indicator) is a plagiarism detector meant to reduce the time taken to calculate level of plagiarism of a document with all the others in a dataset by using concepts of data-parallelism and libraries that work on similar principles

Observations and assumptions so far:

Since an online plag checker would work on a cloud platform, we abandoned local testing in favour of a platform like Colab, as that would give results that are more realistic
Major tests done include comparing the execution time taken by:

Serial implementation (for base time)
Multiprocessing library (for base data-parallelism time)
Psuedo data-parallelism (purely for research purposes)
Numba library (for potential in-built optimum time)
Other libraries, such as iparallel are performing worse than expected, and worse than serial implementation, so they were left out of the final analysis

Numba gives a significant improvement with caching.

Files will be fed as input to the program (to be serially or manually converted beforehand since this project focusses of parallel plagiarism, detection, not conversion)

Final output will consist of two parts from the perspective of:

Product: Dataframe/spreadsheet type structure, showing level of plagiarism between files
Reasearch: A time/speed-up based comparison between the aforementioned methodologies.
Original outcome expected pure data-parallelism to perform better, but that is not the case, hence a black-box implemetation had to be adopted for successful completion.

Input iles are either in .pdf or .txt format

Implementation:

First part involves building the plag-checker and applying the various devised methodologies.
The next step is building a PDF-to-text converter. The goal is to build a simple converter but if time permits, it will be implemented in parallel.
The aim of the project is to create the first two modules.
Since mid-eval: Tested for 50 files, and its time analysis. Added [Max plag value], [Max plag doc], [Average plag] columns to final output. Added multiprocessing file conversion successfully, and time comparison graphs.
