# Uncommon HTML Bug: innerHTML Misuse

This repository demonstrates a subtle but potentially problematic error in using `innerHTML` to add content to an HTML element.  Improper use of `innerHTML` can lead to unexpected behavior, including data loss, security vulnerabilities (XSS), and performance issues.  This example shows both the incorrect approach and the correct, safer alternative.

## The Problem

Repeatedly using `innerHTML += ...` to append new HTML elements can be inefficient and may lead to unintentional loss of data if the element already contains complex HTML structure. It is also a XSS vulnerability if the data is coming from a user.

## The Solution

The correct and safer approach is to use `createElement` and `appendChild`. This method is more performant, less error-prone, and avoids the security risks associated with `innerHTML`.

## Usage

1. Clone this repository.
2. Open `bug.html` in your web browser to see the incorrect usage and its consequences.
3. Open `bugSolution.html` to see the correct implementation using `createElement` and `appendChild`.

## Learning Objectives

* Understanding the limitations of using `innerHTML` for dynamic content updates.
* Learning the preferred method for adding elements using `createElement` and `appendChild`.
* Avoiding potential security risks associated with improper use of `innerHTML`.