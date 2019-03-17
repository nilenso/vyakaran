# TESTING

## Intro

Arrange
Act
Assert

http://wiki.c2.com/?ArrangeActAssert

## Values

- models vs. stubs - what is "testing purity"?
- builders or factories `(create :deposit 20)`
- deepEqual (by-ref vs. by-value)

## Testing evil

- db access / filesystem
- async
- date/time

## Testing purity

- "object-oriented programming" is about *messages* and *message passing*

## The testing pyramid

![alt text](testPyramid.png)
