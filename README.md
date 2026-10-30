# ☕ Java Assignment 4: House Robber Simulation

A Java program that solves several variations of the classic **House Robber** dynamic programming problem, structured with an abstract class.

![Java](https://img.shields.io/badge/Java-ED8B00?logo=openjdk&logoColor=white)

## 🧠 Design

An abstract `Robber` class declares the problem variations, and `JAVAProfessionalRobber` implements them:

| Method | Problem |
|---|---|
| `RowHouses(int[])` | Houses in a row: maximize loot without robbing two adjacent houses |
| `RoundHouses(int[])` | Houses in a circle: the first and last houses are also adjacent |
| `SquareHouse(int[])` | Houses arranged in a square |
| `MultiHouseBuilding(int[][])` | Several buildings, each with its own set of houses |

The row version uses the standard recurrence `dp[i] = max(dp[i-1], dp[i-2] + houses[i])`. The circular version solves the row problem twice, once without the first house and once without the last.

## 🚀 Running

```bash
javac RobberySimulation.java
java RobberySimulation
```
