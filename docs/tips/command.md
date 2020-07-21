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
`--exclude-dir={.directory1,directory2}`

## find

### option

## grep + find

`find folder -type f | xargs grep pattern`  
`find ./ -name '*' | xargs grep hogehoge`


## less

### option

`-i` --ignore-case
`-M` --LONG-PROMPT

## files

### copy and paste file contents to clip board

`pbcopy < hoge1.txt`
`pbpaste > hoge2.txt`
