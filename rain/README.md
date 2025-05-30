# 🌧️ Rainwater Retention Calculation - ALU Interview Project  
**Directory**: `rain/`  
**File**: `0-rain.py`  

## Overview

This project solves the classic problem of calculating how much rainwater can be retained between walls represented by a list of non-negative integers. Each integer corresponds to the height of a wall with unit width, and the goal is to compute how many square units of water can be trapped after it rains.

## Requirements

- Must use Python 3 (specifically version 3.4.3)
- No external modules are allowed (no imports)
- Code must follow **PEP 8 style guide**
- The script must be executable
- A `README.md` at the root of the folder is mandatory

## Function Specification

### Function: `rain(walls)`

- **Prototype**: `def rain(walls)`
- **Parameters**:
  - `walls`: List of non-negative integers representing wall heights.
- **Return**:
  - Integer indicating total amount of rainwater retained.
- **Edge Cases**:
  - Returns `0` if the list is empty.
  - Assumes no walls beyond the ends of the list.

## Approach

The algorithm follows a two-pass dynamic programming method:

1. Compute the maximum wall height to the left of each position.
2. Compute the maximum wall height to the right of each position.
3. For each position, calculate the water retained as:
