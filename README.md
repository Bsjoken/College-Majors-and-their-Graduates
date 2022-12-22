# College-Majors-and-their-Graduates
## The reason behind this dataset is that it helps differentiate college majors and the salary that comes with it after graduation. With the data that we have we will be using four tables(Ages, Grad students, Majors, and Grads to figure out; 
### -What major is employed, unemployed, and the median salary?
### -What's the highest paying major after graduation?
### -What's the comparison between highest salary vs lowest salary after graduation?
### -What's the 25th percentile salary for people that graduated vs 25th perecentile salary for people that didn't graduate?
### 


#### -First we're going to use the data from the `college-majors.All_ages.Ages` dataset to find out what major is employed, unemployed and the median salary. 

SELECT DISTINCT Major, Employed, Unemployed, Median
FROM `college-majors.All_ages.Ages`

#### -What's the highest paying major after graduation?

SELECT Grad_P75, Major, Grad_employed
FROM `college-majors.Grad_Students.Grad students`
ORDER By 1, 2, 3

RESULTS: ![image](https://user-images.githubusercontent.com/120198393/209213740-d29852b0-21ae-47ba-b538-aea2ce5362e3.jpeg)
