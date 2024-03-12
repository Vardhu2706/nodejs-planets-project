# Habitable Planets Identifier

This Node.js program utilizes the Kepler space telescope data to identify potentially habitable planets. It filters through the dataset to find planets that may support life based on specific criteria.

## Features

- **Data Parsing**: Uses the `csv-parse` library to read and parse data from a CSV file named `kepler_data.csv`.
- **Habitability Criteria**: A planet is considered potentially habitable if it meets the following conditions:
  - The Kepler Object of Interest (KOI) disposition is confirmed.
  - The insolation flux (koi_insol) is within the range of 0.36 to 1.11, suggesting Earth-like stellar energy received.
  - The planet radius (koi_prad) is less than 1.6 times Earth’s radius, indicating a likely terrestrial planet.

## Workflow

1. The program reads the `kepler_data.csv` file, which contains the Kepler space telescope findings.
2. It streams the data line by line, applying the `isHabitable` filter function to each planet.
3. Planets that meet the habitability criteria are stored in the `habitablePlanets` array.
4. Upon completing the data processing, it logs the names and the total count of habitable planets found, followed by a completion message.

## Output

- A list of names of the potentially habitable planets.
- The total number of habitable planets identified in the dataset.
- A confirmation message indicating the end of data processing.

Similar programs assists astronomers and astrophysicists in narrowing down the vast Kepler dataset to focus on the most promising exoplanets for further study.
