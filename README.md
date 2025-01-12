# Kotlin's removeIf() Gotcha: Subtle Differences in Collection Behavior

This repository demonstrates a potential issue when using the `removeIf()` function with mutable collections in Kotlin.  The behavior might not be entirely intuitive and can lead to unexpected results depending on the type of collection you're working with (Lists, Sets, Maps).  The example showcases the differences between `removeIf()` on `MutableList`, `MutableSet`, and `MutableMap`.

## Problem

The `removeIf()` function removes elements from a collection based on a predicate. However, depending on the collection type, the iteration and modification might have subtle differences that impact the final result. This can be particularly troublesome when the predicate involves modifying the collection during iteration.

## Solution

The provided solution demonstrates a safe and predictable way to handle element removal, particularly if the predicate might depend on other collection elements or state that gets altered during the removal process.  It usually involves iterating through a copy of the collection or using different filtering and mapping techniques to achieve the desired result without modifying the collection directly during iteration.
