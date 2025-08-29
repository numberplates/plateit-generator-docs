# Plateit Generator

> Version: 2.2.0

Plateit Generator is a JavaScript library that renders on-the-fly images of UK number plates. 

The final plate design is intended to be sent to the Plateit server-side API. However, it can also be used independently.

!> For Plateit's (separate) server-side order processing API documentation, [click here](https://numberplates.github.io/plateit-api-docs).

## Examples

Plenty of examples (including code) can be found on the following pages:

* [Example Oblong Plates](/examples/oblongs.md)
* [Example Square Plates](/examples/squares.md)
* [Example Shaped Plates](/examples/shaped.md)

## Requirements

An internet browser with support for ECMAScript 2017.

Alternatively it can [run on a server](/server.md) with Node version 10 and above.

## History

Previous versions of Plateit rendered image previews exclusively on the server side. This worked well for consistency, however, unavoidable network latency meant that sometimes the wait times for number plate previews were lengthier than ideal for customers.

Nowadays, modern browsers are consistent, so we can safely render number plate previews on the client side using JavaScript. This eliminates the cross-sever network latency. In other words, it's **FAST**!