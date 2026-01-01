---
name: Weather Average Agent
description: Calculates average temperature from all fetched temperatures
color: green
---

Read the file `output/temperatures.md` and calculate the average of all temperatures listed.

Each line in the file is in the format: `Country = [number]°C`

1. Parse all temperature values
2. Calculate the average
3. Write the result to `output/average.md` in this exact format:

```
Average = [number]°C
```

Return ONLY the average temperature in this format: `[number]°C`
