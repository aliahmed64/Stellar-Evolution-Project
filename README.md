# Generating and Assessing Stellar Evolution Models

## Introduction

Stars illuminate through nuclear fusion, converting hydrogen into helium. This process generates energy by turning mass into energy, eventually causing stars to undergo stellar evolution due to limited mass and energy. Stars go through different evolutionary stages, and the main sequence phase is a key period where stars are most stable, burning hydrogen in their cores.

The Hertzsprung-Russell (HR) Diagram is a valuable tool for visualizing stellar evolution by plotting luminosity against color (or temperature). Most stars occupy a specific region known as the main sequence, determined largely by their mass. This project aims to explore the significance of the HR diagram in understanding stellar evolution, how a star's physical parameters determine its position on the diagram, and how mass influences its main-sequence lifetime.

A simplified formula to estimate the main-sequence lifetime ($\tau$) of a star based on its mass ($M$) is:

$$
\tau \approx 10^{10} \left(\frac{M_\odot}{M}\right)^{2.5} \text{ years}
$$

Where $M_\odot$ is the mass of the Sun. This formula provides an approximation but is not universally accurate, primarily designed to match the Sun’s observed main sequence lifetime.

## Methods

1. **Data Collection**: Stellar properties for different stellar masses were downloaded from the EZ-Web database, with all stars having a metallicity value of 0.02. The data files were stored alongside the Jupyter Notebook used for analysis. Python 3.6 was used for this project.

2. **Data Analysis**: Python packages like NumPy, pandas, and matplotlib were used for scientific computing and data visualization. The stellar property data files were imported and stored in appropriately named variables (e.g., `summary_1M`, `summary_2M`), with columns labeled accordingly.

3. **HR Diagram Plotting**: Using functions from the imported libraries, the luminosity and effective temperature of the stars were plotted on HR diagrams. A color bar was used to indicate the star’s age, highlighting the point at which a star leaves the main sequence. An example plot for a 1 solar mass ($1M_\odot$) star was created, and the corresponding code snippet was provided in the project report.

4. **Main Sequence Lifetime Estimation**: The HR diagram was examined to determine the point where each star leaves the main sequence, indicated by changes in color on the diagram. These values were stored in variables (e.g., `tms_1M`) for each star mass.

5. **Lifetime vs. Mass Plot**: Using the estimated main sequence lifetimes, a plot was created showing the relationship between stellar mass and main sequence duration. Observations were made regarding the inverse relationship between mass and main sequence lifespan.

## Results

The study used stars with the following masses: 0.2, 0.4, 0.6, 1.0, 2.0, 4.0, 6.0, 8.0, and 10.0 solar masses. Below are the main sequence lifespans for each mass:

- **$0.2M_\odot$ Star**: ~800,000,000,000 years
- **$0.4M_\odot$ Star**: ~150,000,000,000 years
- **$0.6M_\odot$ Star**: ~50,000,000,000 years
- **$1.0M_\odot$ Star**: ~9,000,000,000 years
- **$2.0M_\odot$ Star**: ~1,150,000,000 years
- **$4.0M_\odot$ Star**: ~175,000,000 years
- **$6.0M_\odot$ Star**: ~62,000,000 years
- **$8.0M_\odot$ Star**: ~32,500,000 years
- **$10.0M_\odot$ Star**: ~21,000,000 years

A comparison table of the HR diagram estimates and the calculated values using the equation above showed that less massive stars (mass < $1M_\odot$) had longer lifetimes than the calculated values, while more massive stars (mass ≥ $1M_\odot$) had shorter observed lifetimes than the calculated estimates.

The plot of stellar main sequence age as a function of stellar mass confirmed an inverse relationship, showing that more massive stars have shorter main sequence lifespans.

## Discussion and Conclusion

The project successfully demonstrated that a star’s main sequence lifetime is inversely proportional to its mass. Massive stars, despite having more hydrogen, burn their fuel at a much faster rate due to higher internal temperatures caused by greater gravitational pressure. Consequently, they spend significantly less time on the main sequence compared to smaller stars.

The HR diagrams and main sequence age vs. mass plots highlighted the critical role of stellar mass in determining a star’s lifespan and evolutionary path. Massive, bright stars live shorter lives, while smaller, fainter stars can remain stable for billions of years.

The following files have been uploaded to this repository:

1. **Project - Data.xlsx**: Contains the collected stellar property data used for analysis.
2. **Stellar Evolution Analysis.ipynb**: Jupyter Notebook file with code and analysis.
3. **summary_0.2M.txt**: Stellar data summary for a star with 0.2 solar masses.
4. **summary_0.4M.txt**: Stellar data summary for a star with 0.4 solar masses.
5. **summary_0.6M.txt**: Stellar data summary for a star with 0.6 solar masses.
6. **summary_1M.txt**: Stellar data summary for a star with 1 solar mass.
7. **summary_2M.txt**: Stellar data summary for a star with 2 solar masses.
8. **summary_4M.txt**: Stellar data summary for a star with 4 solar masses.
9. **summary_6M.txt**: Stellar data summary for a star with 6 solar masses.
10. **summary_8M.txt**: Stellar data summary for a star with 8 solar masses.
11. **summary_10M.txt**: Stellar data summary for a star with 10 solar masses.

## References

- Data Source: [EZ-Web Database](http://www.astro.wisc.edu/~townsend/static.php?ref=ez-web)  
  - Townsend, Rich. "EZ-Web." Mad Star - EZ-Web, 4 Dec. 2021.
