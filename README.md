# Parabatch

A Ruby script to run a simple batch shell script in parallel on a local computer. In the shell script, one line should be corresponding to one independent job.

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
$ cat sample_batch.sh
sleep 1; echo 1
sleep 2; echo 2
sleep 1; echo 3
sleep 3; echo 4
sleep 2; echo 5
sleep 1; echo 6
sleep 2; echo 7
sleep 3; echo 8

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

