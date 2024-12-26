# Unexpected Behavior of removeIf on Mutable List in Kotlin
This repository demonstrates an uncommon bug related to using the `removeIf` function on a mutable list in Kotlin. The `removeIf` function modifies the list in place, which can lead to unexpected behavior if not handled carefully.
The bug occurs because iterating and modifying a list concurrently can result in skipping elements or throwing exceptions. This example showcases how to avoid this error and implement safer list manipulation techniques.
## Bug Description
The provided code intends to remove all even numbers from a mutable list. However, due to the nature of `removeIf`, if not handled properly, it might skip some elements during removal, leading to an incorrect outcome.
## Bug Solution
The solution provides an alternative approach using an iterator or creating a new list for safe modification. This prevents the concurrent modification issue and ensures all even numbers are successfully removed.
## How to reproduce
1. Clone this repository.
2. Open `bug.kt` to see the buggy code.
3. Compile and run the code. Observe that not all even numbers are removed.
4. Open `bugSolution.kt` to see the corrected implementation. 
5. Compile and run the solution code. It will correctly remove all even numbers.
