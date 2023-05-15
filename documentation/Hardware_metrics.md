# Hardware metrics for Dispenser

## 1. Trigger dispenser by hand

- In order to determine the best possible time, the dispenser is operated by hand.

### Empty time (Closed to Open Position)

- Min empty time is 3 s
- Max empty time is 5 s
- With the same actuation, the dispenser empties sometimes faster and sometimes slower.

### Fill time (Opened to Close Position)

- Min fill time is 3 s
- [ ] Further tests would have to be carried out for the optimal filling time, because sporadically the dispenser will not refill,  since problems can arise depending on the speed from the open to closed position

### Best case empty and fill time

- It is possible to empty and refill the dispenser by hand in 6 seconds.

## 2. Trigger dispenser by machine

### Empty and fill time

- With the current software and hardware, it can be done by machine in 18 seconds.
- The empty and fill time are both 9 s
- **Noticed that the dispenser doesn't always refill, even with the slow mechanical actuation**
  - However, with the next emptying, the filling process is completed because of the 9-second actuation time
    - [ ] more tests are needed to verify

### Time for filling a glass with 2 ingredients

| Two Dispenser |     Best-Case fill time (s) | actual fill time (s) |
| ----- | :-------: | :-----------------------: |
| 3 cl (270 ml Drink) |    30  |  90  |
| 4 cl (280 ml Drink) |    24  |  72  |
| 5 cl (250 ml Drink) |  18  | 54 |

- A drink with 2 ingredients currently takes 90 s.
- **With a 5 cl dispenser it would be possible to minimize the time to 54 s**

## Time for filling a glass with 2 cl and 5 cl Dispenser

In the future, 2 cl dispensers could be used for spirits, liqueurs and syrup.
The 50 ml dispenser could be used for other liquids like juices.

The most popular cocktails use an average of 5 ingredients. 3 of them need a quantity of 2 cl each and the remaining 2 of 100 ml each.

**With this configuration, we would need 2 cycles of the dispneser and the time for a drink would be 36 s:**
- First run of the dispenser would make 16 cl
  -  3 x 2 cl = 6 cl
  -  2 x 5 cl = 10 cl
- Second run with the two 5cl dispenser would make 10 cl
