# topsis-102117208

_for: **Predictive Analytics using Statistics (UCS654)**_
_submitted by: **Atanu Mondal**_
_Roll no: **102117208**_
_Group: **3CS-8**_


topsis-3283 is a Python library for dealing with Multiple Criteria Decision Making(MCDM) problems by using Technique for Order of Preference by Similarity to Ideal Solution(TOPSIS).

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install topsis-3283.

```bash
pip install topsis-3283
```

## Usage

Enter csv filename followed by _.csv_ extentsion, then enter the _weights_ vector with vector values separated by commas, followed by the _impacts_ vector with comma separated signs _(+,-)_
```bash
topsis sample.csv "1,1,1,1" "+,-,+,+"
```
or vectors can be entered without " "
```bash
topsis sample.csv 1,1,1,1 +,-,+,+
```
But the second representation does not provide for inadvertent spaces between vector values. So, if the input string contains spaces, make sure to enclose it between double quotes _(" ")_.

To view usage __help__, use
```
topsis /h
```
## Example

#### sample.csv

A csv file showing data for different mobile handsets having varying features.

| Model  | Storage space(in gb) | Camera(in MP)| Price(in $)  | Looks(out of 5) |
| :----: |:--------------------:|:------------:|:------------:|:---------------:|
| M1 | 16 | 12 | 250 | 5 |
| M2 | 16 | 8  | 200 | 3 |
| M3 | 32 | 16 | 300 | 4 |
| M4 | 32 | 8  | 275 | 4 |
| M5 | 16 | 16 | 225 | 2 |

weights vector = [ 0.25 , 0.25 , 0.25 , 0.25 ]

impacts vector = [ + , + , - , + ]

### input:

```python
topsis sample.csv "0.25,0.25,0.25,0.25" "+,+,-,+"
```

### output:
```
      TOPSIS RESULTS
-----------------------------

    P-Score  Rank
1  0.534277     3
2  0.308368     5
3  0.691632     1
4  0.534737     2
5  0.401046     4

``` 

## Other notes

* The first column and first row are removed by the library before processing, in attempt to remove indices and headers. So make sure the csv follows the format as shown in sample.csv.
* Make sure the csv does not contain categorical values


## License
[MIT](https://choosealicense.com/licenses/mit/)