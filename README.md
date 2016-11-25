# :chart_with_upwards_trend: smartR

smartR is a R-based open-source statistical analysis tool for t-test, multi-variate analysis etc.

It can be used as DIY tool for statistical analysis. User can submit his data using web framework and select different options according to his statistical analysis requirement.

The frontend is made through bootstrap framework and the backend in R using openCPU API.
The OpenCPU API defines a mapping between HTTP requests and R function calls which results in a natural RPC protocol. Different types of R statistical packages are used for different types of
analysis. The backend has different methods like data upload, data
summary, statistical test and fetch result.

## Install hack
Follow these instructions to install smartR for single user.
```
install.packages("opencpu")
library(devtools)
install_github("smart_r","namangt68")
library(opencpu)
install_github("smart_r","namangt68")
opencpu$browse("library/smartR/www")
```
## AIM
Design and implement a statistical analysis DIY(Do it yourself) tool that can
be used for primitive statistical analysis for business intelligence etc. Tool
should enable users to do different types of statistical tests on an easy to
use web based platform. 

## Project Plan
1. Know about scope of project and its usefulness to overall business analyst community.

2. Understanding different statistical tests and possible technologies that can be used.
3. Design a project outlay map for execution, compare and decide among different available technologies that can be used to build that product.
4. Setting the work architecture of the project and then its implementation.

## Technology stack

* OpenCPU API( for seamless integration of R and JavaScript)
* Rstudio(for package management)
* R statistical packages(for multivariate analysis etc.)
* Bootstrap(framework for web UI)

## Example analysis
Many different types of analysis are implemented in smart-r. On selecting
different types of analysis different options for argument selection should
be shown (may depend on data uploaded for some analysis). Options for
different analysis types are:

One-Sample t test
* test variable(s) selection
* test value # testing if mean of x could be

Sample Result Display

```
One Sample t-test
data:
x
t = -0.8547, df = 49, p-value = 0.3969
alternative hypothesis: true mean is not equal to 10
95 percent confidence interval:
9.797195 10.081767
sample estimates:
mean of x
9.939481
```

## WorkFlow
Once the user upload his data file using on upload file button a R function
uploaddata is called through OpenCPU api.

The user can select different arguments about data file type and type of
analysis he/she wants to do. The upload data function then again calls for
read and validate data package and then data gets stored on server for
further interpretation.

As per user input respective stastical fucntion is called and data get
intrepreted.Once the statistical tests gets completed, data summary along
with the results are shown on web UI as per user input.

## Future scope
This tool can later be developed into a full fledged business intelligence tool
that can create and distribute interactive dashboards which depict the
trends, variations and density of the data in different forms like graphs etc.
It may allow to connect to big data sources to acquire and process data.


## License

[GPL 3.0](LICENSE)
