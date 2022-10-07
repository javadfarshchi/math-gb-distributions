# math-gb-distribution Package

math-gb-distribution is a Python library for helping you with calculation, plotting, and summation of Gaussian and Binomial Distributions. 

There are two main classes that can be used by the user, Gaussian and Binomial. Gaussain class can take either the data list (.read_data_file('data.txt')) or the mean and standard deviation of the data directly. If the user chooses to load the data from the file, average and standard deviation of the data can be calculated by calculate_mean() and calculate_stdev() methods. The user can calculate the probability density function of the Gaussian distribution at any point 'x' by the pdf(x) method. The histogram of the Gaussian distribution can also be plotted using plot_histogram_pdf(n_spaces), n_spaces being number of data points. The user can also define two separate Guassian distributions and add them together as if they are regular numbers.

For the Binomial distributions, most of the methods are similar to the Gaussian class. There are few differences. The Binomial class takes probability and size as it's input arguments, Binomial(prob (float) , size(float)). All the methods in the Gaussian class are also available for the Binomial distribution class. For the calculation of probability density function, one should use pdf_binomial(k), k being teh point for calculating the probability density function.

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install math-gb-distribution.

```bash
pip install math-gb-distribution
```

## Importing

```python
import math-gb-distribution

```

## Gaussian Class
```python
# Gaussian class takes either average and standard deviation or the data file
Gaussian(mean(float), stdev(float))
or
Gaussian.read_data_file('data.txt')

# Returns average of the data 
Gaussian.calculate_mean()

# Returns standard deviation of the data
Gaussian.calculate_stdev()

# Returns the probability density function of the Gaussian distribution at any point 'x'
Gaussian.pdf(x)

# Returns the histogram of the Gaussian distribution with specified number of spaces
Gaussian.plot_histogram_pdf(n_spaces)

# Simply adding two Gaussian distributions
# Example
gaussian_one = Gaussian(25, 3)
gaussian_two = Gaussian(30, 4)
gaussian_sum = gaussian_one + gaussian_two
```

## Binomial Class

```python
# Binomial class takes either probability and size of the data or the data file
Binomial(prob(float), size(float))
or
Binomial.read_data_file('data.txt')

# Returns average of the data 
Binomial.calculate_mean()

# Returns standard deviation of the data
Binomial.calculate_stdev()

# Returns the probability density function of the Binomial distribution at any point 'k'
Binomial.pdf_binomial(k)

# Returns the barplot of Binomial distribution
Binomial.plot_pdf_binomial(self)

# Simply adding two Binomial distributions (They should have same probabilities)
# Example
binomial_one = Binomial(.4, 20)
binomial_two = Binomial(.4, 60)
binomial_sum = binomial_one + binomial_two

```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://github.com/javadfarshchi/math-gb-distributions/blob/master/math_gb_distributions/license.txt)
