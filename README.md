# Quiz Leaderboard System — SRM Internship Assignment

## Problem Statement
Build an application that polls a quiz API 10 times, deduplicates the event data, aggregates scores per participant, and submits a final leaderboard.

## How It Works
1. Polls the API 10 times (poll=0 to poll=9) with a 5-second delay between each call
2. Deduplicates events using a unique key of `roundId + "_" + participant`
3. Aggregates total scores per participant
4. Sorts leaderboard by totalScore in descending order
5. Submits the leaderboard once via POST request

## Key Design Decisions
- No external libraries — uses Java 11 built-in HttpClient
- Deduplication via HashSet with key = roundId_participant
- 5-second mandatory delay between polls
- Single POST submission at the end

## How to Run
```bash
javac QuizLeaderboard.java
java QuizLeaderboard
```

## Result
Successfully submitted with `attemptCount: 1` and `submittedTotal: 1365`
