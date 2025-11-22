The data/raw/ directory contains 50 unprocessed animal shelter intake data, each file refering to a single day in the format animal_data_YYYYMMDD.

The following columns exist in each file.

Date: Date of data collection (YYYY-MM-DD).
NumOfAnimals: Number of animals in the shelter on that date. Source: web scraping.
average_temp: Average temperature (°F) on that date. Source: AccuWeather API.
Precipitation: Binary indicator—1 if precipitation chance was ≥50%, 0 otherwise. Source: AccuWeather API.
MonthsInCare: Number of months the animal has been continuously in the shelter. Source: web scraping.
AgeInMonths: Age of the animal in months. Source: web scraping.
Season_[Spring/Summer/Fall/Winter]: One-hot encoded season. Derived from date.
DayOfWeek_[Monday-Sunday]: One-hot encoded day of week. Derived from date.
Species_[type]: One-hot encoded species. Columns may vary depending on which species are present on a given day. Source: web scraping.
