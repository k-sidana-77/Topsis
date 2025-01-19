# TOPSIS Implementation

## Program 1: Command Line Implementation
Command to run:
```bash
python <RollNumber>.py <InputDataFile> <Weights> <Impacts> <ResultFileName>
```

Example:
```bash
python 101556.py 101556-data.csv "0.2,0.2,0.2,0.2,0.2" "+,+,+,+,+" 101556-result.csv
```

### Sample Input Data (data.csv)
```
Fund Name,P1,P2,P3,P4,P5
M1,0.84,0.71,6.7,42.1,12.59
M2,0.91,0.83,7.0,31.7,10.11
M3,0.79,0.62,4.8,46.7,13.23
M4,0.78,0.61,6.4,42.4,12.55
M5,0.94,0.88,3.6,62.2,16.91
M6,0.88,0.77,6.5,51.5,14.91
M7,0.66,0.44,5.3,48.9,13.83
M8,0.93,0.86,3.4,37.0,10.55
```

### Sample Output (result.csv)
```
Fund Name,P1,P2,P3,P4,P5,Topsis Score,Rank
M1,0.84,0.71,6.7,42.1,12.59,0.5637,3
M2,0.91,0.83,7.0,31.7,10.11,0.513,4
M3,0.79,0.62,4.8,46.7,13.23,0.4392,6
M4,0.78,0.61,6.4,42.4,12.55,0.492,5
M5,0.94,0.88,3.6,62.2,16.91,0.6419,2
M6,0.88,0.77,6.5,51.5,14.91,0.7381,1
M7,0.66,0.44,5.3,48.9,13.83,0.4074,8
M8,0.93,0.86,3.4,37.0,10.55,0.4085,7
```

### Input Requirements
- Input CSV file must have 3+ columns
- First column: Object names (M1, M2, etc.)
- 2nd column onwards: Numeric values only
- Weights: Comma-separated (e.g., "0.2,0.2,0.2,0.2,0.2")
- Impacts: Comma-separated +/- (e.g., "+,+,+,+,+")

### Error Handling
- Checks for correct parameter count
- File existence verification
- Numeric values validation
- Weights and impacts count validation
- Impact symbols must be + or -
