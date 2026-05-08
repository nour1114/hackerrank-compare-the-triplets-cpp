# Compare The Triplets - HackerRank Solution (C++)

This repository contains my C++11 solution for the HackerRank problem:

🔹 Compare The Triplets

## Problem Overview
Two participants, Alice and Bob, are compared across three categories.  
For each category:
- If Alice's score is higher, Alice gets 1 point.
- If Bob's score is higher, Bob gets 1 point.
- If scores are equal, no points are awarded.

The program returns the final scores for both participants.

## Concepts Used
- C++11
- Vectors
- Loops
- Conditional Statements
- Problem Solving

## Solution
```cpp
#include <bits/stdc++.h>
using namespace std;

vector<int> compareTriplets(vector<int> a, vector<int> b) {
    int alice = 0, bob = 0;

    for (int i = 0; i < 3; i++) {
        if (a[i] > b[i])
            alice++;
        else if (a[i] < b[i])
            bob++;
    }

    return {alice, bob};
}

int main() {
    vector<int> a(3), b(3);

    for (int i = 0; i < 3; i++)
        cin >> a[i];

    for (int i = 0; i < 3; i++)
        cin >> b[i];

    vector<int> res = compareTriplets(a, b);

    cout << res[0] << " " << res[1];

    return 0;
}
```

## HackerRank Profile
hackerrank.com/profile/nourelsali2006
