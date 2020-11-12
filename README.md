# Simulation Tools

## Simulation
- Require:   Output folder exists.
- Effect:    To get the truth table of a logic network (BLIF format).
```
usage: ./bin/Simulate --input=string [options] ... 
options:
  -i, --input     Input Filename (string)
  -o, --output    Output Filename (string [=])
  -?, --help      print this message
```

## Merge
- Require:   AIGs name: 0.aag, 1.aag, 2.aag, ... in the Input directory.
- Effect:    Merge several single-output networks (.aag) into one multi-output network.
```
usage: ./bin/Merge --input=string --number=int --output=string [options] ... 
options:
  -i, --input     Input Directory (string)
  -n, --number    Number of AIGs input (int)
  -o, --output    Output File (string)
  -?, --help      print this message
```

### Split Example
For example, the following folder has `--input ./input/directory` and `--number 5`
```
./input/directory/
    .
    ..
    0.aag
    1.aag
    2.aag
    3.aag
    4.aag
```

## Gen
- Require:   Output Directory exists
- Effect:    Generate train/test dataset (as in the contest) for up to 10 outputs of the given logic network (BLIF format).
```
usage: ./bin/Gen --input=string [options] ... 
options:
  -i, --input     Input Filename <blif> (string)
  -o, --output    Output Directory (string [=])
  -?, --help      print this message
```

## Split
- Require:   Output Directory exists
- Effect:    Generate train/test dataset (as in the contest) for up to 10 outputs of the given logic network (BLIF format).
```
usage: ./bin/Split --input=string [options] ... 
options:
  -i, --input     Input Filename (string)
  -o, --output    Output Directory (string [=])
  -n, --number    Input Number (int [=1])
  -?, --help      print this message
```

### Split Example
For example, the memory banking dataset has `--number 2`
```
#   In1<5> In2<5> Out1<2> Out2<8>
    ...
    31 31 3 255
    ...
```
