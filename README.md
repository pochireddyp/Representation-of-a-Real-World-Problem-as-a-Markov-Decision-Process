# Representation-of-a-Real-World-Problem-as-a-Markov-Decision-Process

## Aim

To represent a real-world traffic signal control system as a Markov Decision Process (MDP) by defining its states, actions, transition probabilities, reward function, and implementing it using Python dictionaries.

---

## Problem Statement

### Problem Description

Consider a traffic signal control system at a road intersection. The traffic signal acts as an agent that decides whether to keep the current signal or switch it to reduce vehicle congestion and waiting time. The objective is to minimize traffic delays and maximize smooth traffic flow.

---

## MDP Components

A Markov Decision Process is represented as:

$$
MDP = (S, A, P, R, \gamma)
$$

Where:

| Symbol | Meaning |
|---|---|
| $S$ | Set of states |
| $A$ | Set of actions |
| $P$ | Transition probability function |
| $R$ | Reward function |
| $\gamma$ | Discount factor |

---

## State Space
The possible traffic conditions are:


Example format:

```text
S = {
    Low Traffic,
    Medium Traffic,
    High Traffic
}
```
---

## Sample State

```text
High Traffic
```
---

## Action Space

Possible actions of the traffic signal are:

```text
A = {
    Keep Green,
    Switch Signal
}
```
---

## Sample Action

```text
Switch Signal
```
---

## Transition Probability

The transition probability defines the chance of moving from one traffic condition to another after taking an action.

Example:

```text
P(Medium Traffic | High Traffic, Switch Signal) = 0.8
```

Meaning:

There is an 80% probability that heavy traffic reduces to medium traffic after switching the signal.

---

## Reward Function

The reward is given based on traffic improvement.
```text
R(s, a, s')
```

Examples:

High Traffic → Medium Traffic = +10
Medium Traffic → Low Traffic = +15
Traffic remains High = -10
Unnecessary signal switch = -2

---

## Graphical Representation

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/112e0625-6a24-493b-842b-4fab924b043f" />

---

## Python Representation


```python
print("Name: POCHI REDDY GARI POCHI REDDY")
print("Register Number: 212223240115")

print("\nStates:")
for state in states:
    print(state)

print("\nActions:")
for action in actions:
    print(action)

print("\nTransition Probabilities:")
for key, value in transition_probability.items():
    print(f"{key} -> {value}")

print("\nRewards:")
for key, value in rewards.items():
    print(f"{key} -> {value}")

print("\nDiscount Factor:")
print(discount_factor)
```
---
## Output


<img width="853" height="558" alt="image" src="https://github.com/user-attachments/assets/a3cf3289-79b9-4fe4-9cb4-84bf13cc593b" />

---

## Result

Thus, the real-world traffic signal control problem was successfully represented as a Markov Decision Process (MDP) by defining its states, actions, transition probabilities, reward function, discount factor, and implementing it using Python.



---

