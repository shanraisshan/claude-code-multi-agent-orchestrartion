# Orchestrate Command

Orchestrates weather agents to fetch temperatures in parallel, then calculates the average.

## Instructions

1. **Launch both weather agents in parallel** using the Task tool:
   - Launch `Weather Pakistan Agent` with prompt: "Fetch the temperature"
   - Launch `Weather India Agent` with prompt: "Fetch the temperature"
   - Run both in background (`run_in_background: true`)

2. **Wait for both agents to complete** using TaskOutput

3. **Launch the Weather Writer Agent** to write results:
   - Launch `Weather Writer Agent` with prompt containing the temperatures:
     "Write these temperatures: Pakistan = [temp1], India = [temp2]"
   - Wait for it to complete

4. **Launch the Weather Average Agent** (sequentially, after temperatures are saved):
   - Launch `Weather Average Agent` with prompt: "Calculate the average temperature"
   - Wait for it to complete

5. **Confirm** both reports have been saved:
   - `output/temperatures.md`
   - `output/average.md`

## Important

- Run weather fetch agents in PARALLEL
- Run Weather Writer Agent AFTER fetching temperatures
- Run Average Agent AFTER temperatures are written
- Output format for temperatures is just two lines
- Output format for average is just one line
