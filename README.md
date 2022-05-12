# pitch-detector
a bash script that uses aubio to detect the pitch of a sample, and renames the file accordingly

usage: 
pitch-detector.sh <inputfile>

outputs:
output/<notename> <inputfile>

example:
$ pitch-detector.sh "my piano sample.wav"
$ ls -l output/
D# my piano sample.wav

example:
$ find . -type f -iname *.wav -exec pitch-detector.sh {} \;
$ ls -l output/

