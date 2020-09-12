---
layout: default
title: Command
parent: Tips
---

# Command
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

Useful commands.

## grep

`grep [-option] pattern file`

### option

`-i` -ignore-case  
`-n` --line-number  
`-r` --recursive  
`-I` –binary-files=without-match  
`--exclude-dir={directory1,directory2}`

## find

### option

## grep + find

`find folder -type f | xargs grep pattern`  
`find ./ -name '*' | xargs grep hogehoge`


## less

### commands

`d` Scroll forward N lines, default one half of the screen size.

`G or > or ESC->`  Go to line N in the file, default the end of the file.

### option

`-i` --ignore-case

`-M` --LONG-PROMPT

## files

### copy and paste file contents to clip board

`pbcopy < hoge1.txt`  
`pbpaste > hoge2.txt`


## ps

### option

`-u` Display user-oriented format  
`ps aux | grep keyword`

## du 

display disk usage statistics

### option

`-c`  Display a grand total.  
`-h`  "Human-readable" output.  Use unit suffixes: Byte, Kilobyte, Megabyte, Gigabyte, Terabyte and Petabyte.  
`-s`  Display an entry for each specified file.  
du -shc ~/*

## hdf

### hdf4

`adp command file`  
`list` Displays the contents of the HDF files in the specified format.  
`dumpsds` Displays the contents of the SDSs in the listed files.  
`dumpvd` Displays the contents of the vdata objects in the listed files.  
`dumpvg` Displays the contents of the vgroup objects in the listed files.  

### hdf5

`h5dump [-option] file`  
`-n` Displays a list of the objects in a file.
`-H` Displays header information only (no data).

