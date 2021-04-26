# DeepSquiggle

To extract squiggle data from nanopore data, the following command can be used:

```
python SquigglePull.py -v --multi -e -p ./My_own_data/ -t 1500,2500 -f pos1 > my_own.tsv
```
This outputs a large file with one read per line. Every value from column 3 onwards is an electrical reading from the cell at x timepoint.


The aim of this project is to develop a neural network that is able to classify bacterial species by their raw 'squiggle' data. This circumvents the need to turn squiggle data into bases and also allows extra data, such as methylation profiles' to be used to differentiate bacterial species.

To accomplish this, squiggle data is sampled to 5000 reads per species and an image is made for each read. Classifying an image rather than the actual squiggle data allows the data to be analysed using very well established image classification neural networks. 


The fastq file (downloaded from R10 Loman source) was mapped 
