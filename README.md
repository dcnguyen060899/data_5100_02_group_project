# Optimizing Cruise Efficiency for Aircraft Tail 687: Data-Driven Analysis of Altitude and Airspeed Combinations for Fuel Consumption Reduction

## DATA 5100 - Fall Quarter 2025 - Group Project

### Team Members
- Duy Nguyen
- Hemant
- Prithika

### GitHub Repository
[https://github.com/dcnguyen060899/data_5100_02_group_project](https://github.com/dcnguyen060899/data_5100_02_group_project)

## Project Purpose

This project analyzes NASA DASHlink flight recorder data from 312 commercial flights to identify the optimal altitude and airspeed combinations for minimizing fuel consumption during cruise flight. By leveraging statistical modeling and exploratory data analysis on 1.88 million measurements, we provide actionable recommendations for fuel efficiency improvements that could save airlines millions of dollars annually while reducing environmental impact.

## Project Overview

Aircraft Tail 687 consumes thousands of pounds of jet fuel per flight, translating to tens of thousands of dollars in operating costs and substantial carbon dioxide emissions. The aviation industry operates on razor-thin profit margins where even marginal efficiency improvements compound into millions of dollars in annual savings across a fleet. This project leverages NASA's DASHlink database containing detailed flight recorder data from six hundred fifty-two commercial flights to identify operational factors that airlines can control to reduce fuel consumption during cruise flight.



## Research Question

**How do altitude and airspeed combinations affect fuel efficiency during cruise flight for Aircraft Tail 687, and what represents the optimal cruise profile for different operational conditions?**

This question focuses our analysis on actionable operational decisions that pilots and flight planners control directly. Rather than simply identifying correlations between various factors and fuel consumption, we aim to provide specific guidance about altitude selection and speed management strategies that maximize efficiency. Our approach acknowledges that optimal operating conditions likely vary with contextual factors including wind patterns and aircraft weight, requiring adaptive rather than universal optimization strategies.

## Why This Matters

Commercial aviation fuel costs represent approximately thirty percent of total operating expenses for major carriers. A five percent reduction in fuel consumption during cruise flight would generate substantial financial benefits while simultaneously reducing environmental impact. For a typical wide-body aircraft flying transcontinental routes, this translates to approximately fifteen hundred dollars saved per flight and roughly one ton less carbon dioxide emitted. Scaled across a fleet operating thousands of flights annually, such improvements justify significant investment in data-driven optimization systems.

Beyond direct cost savings, fuel efficiency improvements enhance airline competitiveness in an increasingly environmentally conscious market. Regulatory pressure to reduce aviation emissions continues intensifying globally, making proactive efficiency gains both economically prudent and strategically necessary for long-term operational sustainability.

## Data Source and Analytical Dataset

NASA's DASHlink database provides comprehensive flight recorder data from Aircraft Tail 687, a commercial wide-body aircraft instrumented for research purposes. The database contains six hundred fifty-two complete flights recorded and published in 2012, capturing operational data across diverse routes, seasons, and atmospheric conditions. Each flight file contains time-series measurements from the aircraft's flight data recorder, documenting one hundred eighty-six different parameters sampled at varying frequencies throughout the flight envelope.

Our preliminary screening of the complete database revealed that three hundred twelve flights, representing forty-eight percent of the total, reached cruise altitude above twenty-five thousand feet. The remaining flights consisted of shorter regional operations that never entered typical cruise conditions. To maximize statistical power and capture the full range of operational scenarios including rare events and edge cases, we incorporated all three hundred twelve cruise-capable flights into our analytical dataset rather than sampling a subset.

After applying our cruise phase definition and data quality filters, our final analytical dataset comprises one million eight hundred eighty-two thousand five hundred seventy-three individual measurements. At four samples per second, this represents approximately one hundred thirty hours of cruise flight time distributed across diverse operational conditions. This substantial dataset provides robust statistical power to detect operationally meaningful relationships between flight parameters and fuel consumption while capturing sufficient variation to support reliable inference about optimal operating strategies.

### Data Source
- **Primary Source:** NASA's DASHlink Database - Aircraft Tail 687 Flight Recordings
- **Database Link:** [NASA DASHlink Database](https://c3.nasa.gov/dashlink/projects/85/)
- **Publication Date:** 2012
- **Original Dataset:** 651 complete commercial flights

### Data Description
The dataset consists of time-series flight recorder data from a commercial wide-body aircraft (4 engines). Each flight contains measurements of 186 different parameters sampled at varying frequencies throughout the flight envelope.

### Processed Dataset
- **Total Measurements:** 1,882,573 individual data points
- **Flights Included:** 312 flights that reached cruise altitude (>25,000 ft)
- **Flight Duration:** ~130 hours of cruise flight data
- **Sampling Rate:** 4 Hz (4 measurements per second)
- **Key Parameters (32 total):** Altitude, Mach number, true airspeed, fuel flow (4 engines), engine power (N1, N2), exhaust gas temperature, wind conditions, angle of attack, and derived metrics

### Data Files in Repository
- `data/cruise_flight_summary.csv` - Flight metadata (flight names and cruise indicators)
- `data/flight_parameters_dictionary.csv` - Parameter definitions and descriptions
- `data/cleaned_cruise_dataset.csv` - Cleaned analytical dataset (1.88M rows, 32 variables)
