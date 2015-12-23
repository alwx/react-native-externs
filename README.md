# react-native-externs

Google Closure extern files for React Native itself and for the
libraries around it

## Why?

In short there are still benefits from doing advanced optimization.

One of the advantages of React Native is hot release (= ability to
deploy new version without AppStore review). Here simple ClojureScript
application with Om-Next:

|  Optimisation level    |  Size      | Size (gzip best)      |
|------------------------|----------- |-----------------------|
|  `simple`              | 1.1MB      | 148KB                 |
|  `advanced`            | 169KB      | 43KB                  |

The difference would be bigger for the real app which includes
different libraries, etc. Imagine that you have 100k users and you do
weekly release, calculate the traffic.

Another reason for the advanced optimisation - it's really good
obfuscator. With React Native all your source code is available in the
app bundle and it's dramatically easy to replicate the app. With
advanced optimisations it's much easier to write software from scratch
rather than steal the source and try to go through all the garbage
from Google Closure

## Status

Pretty much work in progress - feel free to make pull requests.

## Installation

Download the file and point Google Closure compiler to the folder with externs (`:compiler :exters` for CLJS)

## Keep it up to date

TODO: Put it in NPM and CLJSJS