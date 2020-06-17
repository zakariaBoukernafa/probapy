# probapy
[![PyPI version](https://badge.fury.io/py/probapy.svg)](https://badge.fury.io/py/probapy)

probapy is a Python library for calculating probability density function of a Gaussian or a  binomial distribution

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install probapy.

```bash
pip install probapy
```

## Usage

```python
import probapy
#gaussian 
gaussian = Gaussian(25, 2)
gaussian.read_data_file('numbers.txt')
mean = gaussian.calculate_mean()
stdev = gaussian.calculate_stdev()
pdf = gaussian.pdf(25)


gaussian_one = Gaussian(25, 3)
gaussian_two = Gaussian(30, 4)
gaussian_sum = gaussian_one + gaussian_two #sum of 2 or more Gaussian distributions

#binomial
binomial = Binomial(0.4, 20)
binomial.read_data_file('numbers_binomial.txt')
mean = binomial.calculate_mean()
stdev = binomial.calculate_stdev()

binomial.replace_stats_with_data()
pdf = binomial.pdf(5)

binomial_one = Binomial(.4, 20)
binomial_two = Binomial(.4, 60)
binomial_sum = binomial_one + binomial_two #sum of 2 or more binomial distributions
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)
