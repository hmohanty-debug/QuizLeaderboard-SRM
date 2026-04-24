# Quiz Leaderboard System — Internship Assignment

## Problem Statement
To build an application that polls a quiz API 10 times, handles duplicate event data, adds scores per participant, and submits a final leaderboard.

## How I approached it
1. Polls the API 10 times (poll=0 to poll=9) with a 5-second gap between each call
2. Used a HashSet with `roundId + "_" + participant` as the key to skip duplicates
3. Added up scores per participant
4. Sorted the leaderboard by totalScore in descending order
5. Submitteds the final leaderboard once via POST request

## Why I built it this way
- Didn't use any external libraries — used Java 11's built-in HttpClient
- The deduplication logic was the main challenge since the same event could show up in multiple polls
- Single POST submission at the end 

## How to Run
```bash
javac QuizLeaderboard.java
java QuizLeaderboard
```

## Result
Successfully submitted with `attemptCount: 1` and `submittedTotal: 1365`
