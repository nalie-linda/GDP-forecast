# GDP-forecast

In this project, I analyze data from Pandas Datareader library on the World Bank's Development indicators.
URL--> https://pandas-datareader.readthedocs.io/en/latest/readers/world-bank.html

"""
    Download data series from the World Bank's World Development Indicators

    Parameters
    ----------
    indicator: string or list of strings
        taken from the ``id`` field in ``WDIsearch()``
    country: string or list of strings.
        ``all`` downloads data for all countries
        2 or 3 character ISO country codes select individual
        countries (e.g.``US``,``CA``) or (e.g.``USA``,``CAN``).  The codes
        can be mixed.

        The two ISO lists of countries, provided by wikipedia, are hardcoded
        into pandas as of 11/10/2014.
    start: int
        First year of the data series
    end: int
        Last year of the data series (inclusive)
    freq: str
        frequency or periodicity of the data to be retrieved (e.g. 'M' for
        monthly, 'Q' for quarterly, and 'A' for annual). None defaults to
        annual.
    errors: str {'ignore', 'warn', 'raise'}, default 'warn'
        Country codes are validated against a hardcoded list.  This controls
        the outcome of that validation, and attempts to also apply
        to the results from world bank.
        errors='raise', will raise a ValueError on a bad country code.
    kwargs:
        keywords passed to WorldBankReader

    Returns
    -------
    data : DataFrame
        DataFrame with columns country, year, indicator value
    """
