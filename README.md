![](https://github.com/Alimomeni2000/Brazil-Car-Prices/blob/main/PlotFile/carYearModelPlot.png)


About Dataset

Average car price in Brazil


Data extracted from FIPE.

Every observation (row) corresponds to a average car price, calculated to a month of a year of reference. In other words, in a year (year_of_reference) there are 12 observations related to the same car, however avg_price_brl might differ.

The variables fuel, gear and engine_size were extracted from values of column model, as in original there is no column dedicated to those values. Since some values for model don't contain the information of engine size, this dataset doesn't contain the whole data from FIPE's original. Additionally, if 'Aut.' is not present in model, the car is assumed to be manual.

The prices are calculated by FIPE and they're here as original (in BRL).

FIPE updates the information on a monthly basis. Here, the referred month is given as month_of_reference, as the corresponding year has variable named as year_of_reference

The FIPE codes (fipe_codes) are the model identifier used in FIPE webpage.
Variables

    year_of_reference: year of reference of the observation, i.e., the year the data corresponds to.
    moth_of_reference: month of reference of the observation, i.e., the month the data corresponds to. The average price is calculated by FIPE each month.
    fipe_code: unique id corresponding to a model for easy search on FIPE webpage.
    authentication: unique code that authenticates the consult in FIPE's site.
    brand: car's make.
    model: a description of the car containing the name and other descriptive information, as provided in FIPE table.
    fuel: fuel used by the car. Some of gas cars are actually alcohol and gas (totalflex), which is common in Brazil.
    gear: the way gears are shifted.
    engine_size: Engine size measured in cubic centimeters.
    year_model: those values corresponds to the year of reference, and may not be the same of the year of manufacture, which in case will corresponds to a year before year_model. Observations with year_model = year_of_reference mean the car is brand new for that year of reference, i.e., a 2021 car with year_of_reference = 2021 and moth_of_reference = July mean that the observation (mainly the average price) corresponds to a brand new car in the year of 2021, of the month of July. The same model may have a different average price for different month.
    avg_price_brl: average car's price, as measured by FIPE, in BRL.

- (variable deleted in Version 2).
Questions

Here are some questions that may be used as starting point of analysis.

    How average prices depend on car's age?
    How the engine size contribute to the average price?
    Can FIPE's prices be used to predict car prices?
    Gather some data from real stores. Can you compute you own average? How's it different from FIPE's?
    Build a time series and make explore them accordingly to engine size and gear type.
    Scale prices with Brazil's minimum wage in order make analysis period wise.`
