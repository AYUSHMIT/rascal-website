---
title: "analysis::statistics::Correlation"
---

#### Usage

`import analysis::statistics::Correlation;`


#### Synopsis

Correlation between data values.

#### Description

Compute the http://en.wikipedia.org/wiki/Correlation[correlation] between pairs of data values.
Correlation measures the statistical relationship between two sets of data.

The following functions are provided:
* [Library:function:analysis::statistics::Correlation::Pearsons correlation](/docs//Library/analysis/statistics/Correlation#analysis::statistics::Correlation-PearsonsCorrelation)
* [Library:function:analysis::statistics::Correlation::Pearsons correlation p values](/docs//Library/analysis/statistics/Correlation#analysis::statistics::Correlation-PearsonsCorrelationPValues)
* [Library:function:analysis::statistics::Correlation::Pearsons correlation standard errors](/docs//Library/analysis/statistics/Correlation#analysis::statistics::Correlation-PearsonsCorrelationStandardErrors)
* [Library:function:analysis::statistics::Correlation::Spearmans correlation](/docs//Library/analysis/statistics/Correlation#analysis::statistics::Correlation-SpearmansCorrelation)
* [Library:function:analysis::statistics::Correlation::covariance](/docs//Library/analysis/statistics/Correlation#analysis::statistics::Correlation-covariance)


## function PearsonsCorrelation {#analysis-statistics-Correlation-PearsonsCorrelation}

* ``num PearsonsCorrelation(lrel[num x,num y] values)``


#### Synopsis

Pearson product-moment correlation coefficient.

#### Description

Compute the http://en.wikipedia.org/wiki/Pearson_product-moment_correlation_coefficient[Pearson product-moment correlation coefficient].
It is a measure of the strength of the linear dependence between two variables.

#### Pitfalls

Use [Spearmans correlation](/docs//Library/analysis/statistics/Correlation#analysis::statistics::Correlation-SpearmansCorrelation) when there is a *monotonous dependence* between the two variables.

## function PearsonsCorrelationStandardErrors {#analysis-statistics-Correlation-PearsonsCorrelationStandardErrors}

* ``list[real] PearsonsCorrelationStandardErrors(lrel[num x,num y] values)``


#### Synopsis

Standard errors associated with Pearson correlation. 

## function PearsonsCorrelationPValues {#analysis-statistics-Correlation-PearsonsCorrelationPValues}

* ``list[real] PearsonsCorrelationPValues(lrel[num x,num y] values)``


#### Synopsis

P-values (significance) associated with Pearson correlation.

## function SpearmansCorrelation {#analysis-statistics-Correlation-SpearmansCorrelation}

* ``num SpearmansCorrelation(lrel[num x,num y] values)``


#### Synopsis

Spearman's rank correlation coefficient.

#### Description

Compute http://en.wikipedia.org/wiki/Spearman's_rank_correlation_coefficient[Spearman's rank correlation coefficient].
The correlation between the data values is computed by first performing a rank transformation
on the data values using a natural ranking and then computing [Pearsons correlation](/docs//Library/analysis/statistics/Correlation#analysis::statistics::Correlation-PearsonsCorrelation).

#### Pitfalls

Use [Pearsons correlation](/docs//Library/analysis/statistics/Correlation#analysis::statistics::Correlation-PearsonsCorrelation) when there is a *linear dependence* between the variables.

## function covariance {#analysis-statistics-Correlation-covariance}

* ``num covariance(lrel[num x,num y] values)``


#### Synopsis

Covariance of data values.

#### Description

Computes the http://en.wikipedia.org/wiki/Covariance[covariance] between the `x` and `y` values.

#### Examples


```rascal-shell
rascal>import analysis::statistics::Correlation;
ok
rascal>covariance([<1,12>,<3,12>,<3,11>,<5,7>]);
num: -2.5
```

