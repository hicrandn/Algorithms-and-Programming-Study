# Language Detection Algorithm

## Overview

This project is an Algorithm and Programming practice project that detects whether a given text is written in English or German.

The user enters a text with a maximum length of 3000 characters. The program cleans unwanted characters from the input, calculates the frequency of bigrams and trigrams, and compares the results with predefined English and German frequency data to determine the language of the text.

## Features

- Takes text input from the user.
- Removes foreign and unsupported characters.
- Calculates bigram and trigram frequencies.
- Uses Euclidean distance to compare text patterns.
- Detects whether the text is English or German.

## Implementation Steps

### Step 1: Text Input and Frequency Analysis

- The `gets()` function is used to receive text input from the user.
- The frequency of predefined English and German bigrams and trigrams is calculated.

### Step 2: Text Filtering

- The `void filter_str(char[])` function is used to clean unwanted characters.
- Each character in the char array is checked individually.
- Characters other than uppercase letters (A-Z), lowercase letters (a-z), and spaces (ASCII: 32) are replaced with spaces.

### Step 3: Bigram and Trigram Frequency Calculation

- The `void calculate_frequencies_bi(char str[])` function calculates how many times each bigram appears in the input text.
- The calculated frequencies are stored sequentially in the `calculated_frequencies[]` array.

- The `void calculate_frequencies_tri(char str[])` function calculates trigram frequencies.
- The results are stored starting from the 10th index of the `calculated_frequencies[]` array.

### Step 4: Distance Calculation

- The `void calculate_distances()` function calculates Euclidean distances.

- The calculated text frequency values are compared with:
  - `frequencies_eng[]` → English language frequency matrix
  - `frequencies_germ[]` → German language frequency matrix

- The calculated distances are stored in the global `distances[]` array.

### Step 5: Language Detection

- The `void detect_lang()` function compares `distances[0]` and `distances[1]`.

- If the English distance is smaller, the text is classified as English.
- Otherwise, it is classified as German.

## Technologies

- C Programming Language
- Algorithm Design
- String Processing
- Frequency Analysis
- Euclidean Distance Calculation

## Purpose

The aim of this project is to practice algorithm development, string manipulation, and basic language detection techniques using frequency analysis.
