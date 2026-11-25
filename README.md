# Half Marathon Sub-2 Simulator

A small, interactive what-if tool for exploring how training assumptions could affect a half-marathon finish time. The starting scenario uses a recent long-run pace of **10:45/mi**, three runs per week, and ten weeks until race day.

## Run it

Open [`index.html`](./index.html) in a modern web browser. The project is a standalone page: no dependencies, build step, or server are required.

## Use the simulator

Adjust the sliders and the projected finish time, race-day pace, and progression chart update immediately.

- **Weeks until race day:** 4–16 weeks
- **Training runs per week:** 2–5 runs
- **Weekly pace improvement:** 0–12 seconds per mile

Use the **Miles / Kilometers** buttons to switch pace units. **Reset** returns to the starting scenario. **Export Plan** downloads the current scenario as a text file.

## How the estimate works

The simulator assumes your recent long-run pace is the starting pace, then applies a constant weekly improvement:

1. Adjust the selected pace improvement for training frequency:  
   `weekly improvement × sqrt(runs per week ÷ 3)`
2. Subtract that improvement multiplied by the number of weeks from the starting pace.
3. Multiply the projected pace by the half-marathon distance (**13.1094 mi**) to estimate finish time.

This is a simplified scenario model, not a training plan or a prediction. It assumes linear progress and does not account for factors such as recovery, injury, course conditions, or race-day performance. Use it to explore assumptions, not as medical or coaching advice.
