# College-Majors-and-their-Graduates
### The reason behind this dataset is that it helps differentiate college majors and the salary that comes with it after graduation. With the data that we have we possess five tables of data that goes into depth about the college majors and the salaries that it produces. 

#### First we're going to use the data from the `college-majors.All_ages.Ages` dataset to find out what major is employed/unemployed and the median salary. 

SELECT DISTINCT Major, Employed, Unemployed, Median
FROM `college-majors.All_ages.Ages`

Next we want to figure out the median salary for people that were in employed with the major Accounting.

SELECT Median, Major, Employed
FROM `college-majors.All_ages.Ages`
WHERE Major = 'ACCOUNTING'
