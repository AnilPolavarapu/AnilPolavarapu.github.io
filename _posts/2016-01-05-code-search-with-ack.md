---
layout: post
title: Code search in a linux shell
---

There are times when I have to search for code in a bash shell and cannot connect my IDE to that machine in some way. I end up using a combination of find and grep utilities to get the job done.

For example, to find all java files which have the word responseCode in them I use this.

<code>find <path of code base> -name “*.java” | xargs grep responseCode</code>


I find this repetitive and many developers have created aliased around this to hide the long syntax/avoid typing.

For example, you can add this to your bashrc (or equivalent in your OS)

<code>alias fj=’find <path of code base> -name “*.java” | xargs grep’</code>

Aliases make this bearable but still pretty ugly as this does not give you contextual information of the search term, if you need that you have to resort to using -A (after) and -B (before) flags in grep.

The other day I found a nice tool which can do this work for me. Its called ack.

You can install this using your OS specific package manager. In my setup it is as simple as sudo yum install ack

Here’s how ack listing looks like, arguably prettier and useful than bare bones find&grep.

The man page of ack says this and so far it is living up to expectations.

*DESCRIPTION
Ack is designed as a replacement for 99% of the uses of grep.*

### Installing ack

If you are on Ubuntu, you can use apt in this way.

sudo apt-get install ack

### Usage

ack -i responsecode