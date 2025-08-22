# Drone Delivery
Your solution should run once for all test files located in the TestData directory.

## Sample Input Format
Test files contain orders with coordinates for delivery locations, along with a location for a distribution center and the number of available drones:
```json
{
  "orders": [
    {"orderId": 1, "latitude": 32.7767, "longitude": -96.7970},
    {"orderId": 2, "latitude": 32.7831, "longitude": -96.8067},
    {"orderId": 3, "latitude": 32.7901, "longitude": -96.8004},
    {"orderId": 4, "latitude": 32.7755, "longitude": -96.7892},
    {"orderId": 5, "latitude": 32.7889, "longitude": -96.7956}
  ],
  "distributionCenter": {"latitude": 32.7767, "longitude": -96.7970, "numberDrones": 2}
}
```

## Sample Output Format
For each test file, save a solution file with the following contract:
```json
{
  "route": [
    {
      "droneId": 1,
      "packageIds": [ 1, 2 ],
    },
    {
      "droneId": 2,
      "packageIds": [ 3, 4, 5 ],
    }
  ]
}
```

Each route should be one instance of a drone leaving the distribution center to deliver orders in the specified sequence before returning to the distribution center.  The solutions should be saved with the same name, in the Solutions directory.
