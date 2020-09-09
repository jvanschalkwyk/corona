# corona

R routines that manipulate and display publicly available data about the Novel Coronavirus 
(SARS-CoV-2) and COVID-19. Most of the data are derived from Our World In Data, but publicly available
death data from several countries are also used. 

Other illustrative programs and data are used to contextualise the coronavirus. I've also
written a book (as yet unpublished) called `Rona: the autobiography of a virus` that explores
the data in more depth and provides a rich social context. 

Once installed (see below), from the R console say:

```R
?corona
```

You can similarly look up each function. Important examples are: 


* `corona_country('New Zealand')`: This graphs both cases and deaths per day for the chosen
   country, but also provides smoothed curves. The "5x death" curve is of special interest,
   as it highlights differences between countries. Contrast 'France' and 'Germany', for
   example. For a list of countries, specify '?'. 

* `country_dead()`: Weekly deaths for various countries. Defaults to 'England+Wales', but
   you can use the '?' parameter to get a list here too. Three sequential panels are
   displayed, first the raw data, then with early adjustment for secular change, and
   finally a control chart (created using *qicharts2*) that crudely adjusts for seasonal
   variation, revealing the death spike where this is prominent. (In contrast, in New Zealand,
   there is a 'death dip'). 

Several other functions are available for exploring the context of the coronavirus. Some
of these may at first glance seem irrelevant, but the book _Rona_ ties them together in
a rich social context. Topics covered include exponential growth (corona_rabbits), Bayesian
decision making and the Monty Hall problem (corona_monty), the use of run charts to explore
hand sanitisation and Semmelweis' death data (corona_vienna), power laws (corona_metabolism)
and how statistical distributions arise (corona_converge), with some notes on Benford's law. 

## Installation

```R
# Install the development version from GitHub
devtools::install_github("jvanschalkwyk/corona")
```

-----
