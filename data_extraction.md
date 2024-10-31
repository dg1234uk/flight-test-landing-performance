# Extracting Flight Test Data

```python
# Load in complete data set
df = pd.read_excel("demo_data/L39_flight1-221209-114646.xlsx")

# Find time slice of interest
# This will plot altitude against index number
alt = df["ASL"]
alt.plot()
plot.show()

# Slice indices you want
df_landing = df[33500:] # From index 33500 to the end

# Confirm it's what you want
alt = df_landing["ASL"]
alt.plot()
plot.show()

# Save to new excel file
df_landing.to_excel("demo_data/landing.xlsx", index=False)

# Now you can just load that file to save on load time etc.
```