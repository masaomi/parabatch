# Parabatch

A Ruby script to run a simple batch shell script in parallel on a local computer.

# Usage

```
$ ruby parabatch.rb
Usage:
 ruby parabatch.rb [batch.sh] [threads] ([out.dat]) 2> err.log 
```

# Requirements (gem)

* parallel 
* ruby-progressbar

# Exmaple

```
$ ruby parabatch.rb sample_batch.sh 1
Time: 00:00:15 =================================================================================================================== 100% Progress

$ ruby parabatch.rb sample_batch.sh 8
Time: 00:00:03 =================================================================================================================== 100% Progress

$ cat out.dat
1
2
3
4
5
6
7
8
```

