# CAISO_data

The CAISOdata.csv file contains 5-minute resolution data for supply, demand, and emissions in the CAISO balancing authority. This csv file was created using the script found at https://github.com/grgmiller/CAISO_operations. I will attempt to publish updates to this CSV file on a regular basis. 

# Description of Data
Column Name | Description | Column Format | Data Unit
--|--|--|--
date | Date | MM/DD/YYYY | N/A
month | Month number (1-12) | integer | N/A
day | Day Number (1-31) | integer | N/A
weekday | Day of Week (0-6, where 0 = Sunday) | integer | N/A
hour | Hour number (0-23) | integer | N/A
interval | 5-min interval within each our (1-12, where 1 = 5-min period ending H:05) | integer | N/A
5min_ending | 5-min interval end time (e.g. 03:10 is the period from 03:05 to 03:10) | HH:MM | N/A
demand_DayAF | Day-ahead demand forecast | integer | MW
demand_HourAF | Hour-ahead demand forecast | integer | MW
demand_actual | Actual demand | integer | MW
demand_net | Net demand (actual demand minus solar and wind supply) | integer | MW
wind_curtail_MW | Wind supply curtailment (this data has a 1-2 month lag) | float | MW
solar_curtail_MW | Solar supply curtailment (this data has a 1-2 month lag) | float | MW
solar_MW | Solar supply | integer | MW
wind_MW | Wind Supply | integer | MW
geothermal_MW | Geothermal supply | integer | MW
biomass_MW | Biomass supply | integer | MW
biogas_MW | Biogas supply | integer | MW
sm_hydro_MW | Small hydro supply | integer | MW
battery_MW | Battery supply (negative = charging, positive = discharging) | integer | MW
renewable_MW | Sum of all renewable supply (solar, wind, geothermal, biomass, biogas, small hydro, batteries) | integer | MW
natgas_MW | Natural gas supply | integer | MW
lg_hydro_MW | Large hydro supply | integer | MW
imports_MW | Net supply from imports (negative = net exports) | integer | MW
nuclear_MW | Nuclear supply | integer | MW
coal_MW | Coal supply | integer | MW
other_MW | Other supply (petroleum generators) | integer | MW
imports_co2 | Emissions rate from imports | integer | metric Tons CO2 / hr
natgas_co2 | Emissions rate from natural gas | integer | metric Tons CO2 / hr
biogas_co2 | Emissions rate from biogas | integer | metric Tons CO2 / hr
biomass_co2 | Emissions rate from biomass | integer | metric Tons CO2 / hr
geothermal_co2 | Emissions rate from geothermal | integer | metric Tons CO2 / hr
coal_co2 | Emissions rate from coal | integer | metric Tons CO2 / hr

All data downloaded from http://www.caiso.com/TodaysOutlook/Pages/default.aspx
