# Monte Carlo Pi Estimation

## Overview
Monte Carlo simulation estimates complex problems using random sampling and repetition. This implementation estimates π by randomly dropping points in a square containing a quarter circle.

## How It Works

### Setup
- **Unit square**: 1×1 square (area = 1)
- **Quarter circle**: Radius 1, inscribed in the square (area = π/4)

![Unit Square](images/unit_square.png)

### The Process
1. Generate random points (x, y) where 0 ≤ x, y ≤ 1
2. Check if each point falls inside the quarter circle using: x² + y² ≤ 1
3. Count points inside vs. total points

![Circle](images/circle.png)

### Mathematics
Since the quarter circle sits inside the unit square:

```
Points inside circle / Total points ≈ Area of quarter circle / Area of square
Points inside circle / Total points ≈ (π/4) / 1
```

Solving for π:
```
π ≈ 4 × (Points inside circle / Total points)
```

![Ratio](images/ratio.png)
![Pi](images/pi.png)

More sample points = better accuracy.

## Running the Code
```bash
g++ estimating_pi.cpp
./a.out
```

## Key Insight
The beauty of Monte Carlo methods is turning geometric problems into counting problems through random sampling.
