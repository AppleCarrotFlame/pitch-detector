# pitch-detector
a bash script that uses aubio to detect the pitch of a sample, and renames the file accordingly

prerequisites:
```
aubio-tools
```

usage:
```
  $ pitch-detector.sh <inputfile>
```

outputs:
```
  output/<notename> <inputfile>
```

example:
```
  $ pitch-detector.sh "my piano sample.wav"
  $ ls -l output/
  output/D2# my piano sample.wav
```

example:
```
  $ find . -type f -iname *.wav -exec pitch-detector.sh {} \;
  $ ls -l output/
  output/D2# my piano sample_01.wav
  output/E2 my piano sample_02.wav
  output/F2 my piano sample_03.wav
  output/F2# my piano sample_04.wav
  ...
```
