# Sequence-K_Monotonic
This program analyzes a sequence of 10 integers, identifying the number of monotony changes (k) and calculating the maximum and minimum lengths of monotonic subsequences. A sequence is considered k-monotonic if it changes between increasing and decreasing exactly k times.


K-Monotonic Sequence Analysis in C
Overview

This C program analyzes a sequence of 10 integers to determine its monotonic properties. Specifically, it calculates:

  The number of monotony changes (k).
  The maximum and minimum lengths of monotonic subsequences.

A sequence is considered k-monotonic if it changes between increasing and decreasing exactly k times.
Features

  Defensive Programming:
      Ensures the input sequence contains no two consecutive identical elements.
      Prompts the user to re-enter the sequence if invalid input is detected.

  Monotony Analysis:
      Identifies transitions between increasing and decreasing subsequences.
      Tracks the lengths of all monotonic subsequences.

  Output Results:
      Displays the input sequence.
      Reports the number of monotony changes (k).
      Outputs the minimum and maximum lengths of monotonic subsequences.

How to Run

  Clone this repository or download the main.c file.

  Compile the code using a C compiler (e.g., GCC):

gcc -o k_monotonic_sequence main.c

Run the executable:

  ./k_monotonic_sequence

  Follow the on-screen instructions to input the sequence. The program will:
      Prompt for 10 integer inputs.
      Validate the sequence to ensure no two consecutive elements are identical.

  View the analysis results.

Sample Input/Output
Input:

Enter element 1: 1
Enter element 2: 4
Enter element 3: 5
Enter element 4: 9
Enter element 5: 11
Enter element 6: 9
Enter element 7: 8
Enter element 8: 3
Enter element 9: 2
Enter element 10: 15

Output:

The sequence is: [ 1 4 5 9 11 9 8 3 2 15 ]
The given sequence is 3-monotonic.
Minimum length of monotonic subsequences: 2
Maximum length of monotonic subsequences: 5

Key Functions and Logic

  Input Validation:
      Ensures no two consecutive elements in the sequence are the same.
      Uses a do-while loop to enforce valid input.

  Monotony Change Detection:
      Compares the current element with the previous two elements.
      Increments the monotony change counter when a transition is detected.

  Subsequence Length Calculation:
      Tracks the length of each monotonic subsequence.
      Updates the maximum and minimum lengths dynamically.

Dependencies

  C Standard Library (stdio.h).

Future Enhancements

  Extend to support variable sequence lengths.
  Add support for floating-point numbers.
  Implement visualization of monotonic subsequences.
