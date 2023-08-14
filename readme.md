# Plateit Generator

> Version: 1.0.0

Plateit Generator is a Javascript library that renders on-the-fly image previews of UK number plates. **It handles image generation only**. The final plate design is intended to be sent to the Plateit server-side API along with additional order information. However, this is beyond the scope of this documentation.

## Examples

Dozens of examples (including code) can be found on the following pages:

* [Example Oblong Plates](examples/oblongs.md)
* [Example Square Plates](examples/squares.md)

## Requirements

An internet browser with support for ECMAScript 2017.

## History

Previous versions of Plateit rendered image previews on the server side. This worked well for consistency, however, unavoidable network latency meant that sometimes the wait times for number plate previews were lengthier than ideal for customers.

Nowadays, modern browsers are consistent, so we can safely render number plate previews on the client side using Javascript. This eliminates the cross-sever network latency. In other words, it's **FAST**!

## Road Map

The following functionality has been identified for future development:

* Honeycomb plates
* Custom side badges (uploaded by customer)