# College-Majors-and-their-Graduates
## The reason behind this dataset is that it helps differentiate college majors and the salary that comes with it after graduation. With the data that we have we will be using four tables(Ages, Grad students, Majors, and Grads to figure out; 
### -What major is employed, unemployed, and the median salary?
### -What's the highest paying major after graduation?
### -What's the comparison between highest median salary vs lowest median salary after graduation?
### -What's the 25th percentile salary for people that graduated vs 25th perecentile salary for people that didn't graduate? 

## -First we're going to to find out what major is employed, unemployed and the median salary. 

SELECT DISTINCT Major, Employed, Unemployed, Median
FROM `college-majors.All_ages.Ages`
ORDER BY 1, 2, 3, 4


## -What's the highest paying major after graduation?

SELECT Grad_P75, Major, Grad_employed
FROM `college-majors.Grad_Students.Grad students`
ORDER By 1, 2, 3

RESULTS: ![image](https://user-images.githubusercontent.com/120198393/209222868-f2127cbf-2978-4a13-a936-b41b345b9ff9.jpeg)

## -What's the comparison between highest median salary vs lowest median salary after graduation?

SELECT MAX(Median) AS Highest_paid, MIN(Median) AS Lowest_paid
FROM `college-majors.All_ages.Ages`

RESULTS: ![image](https://user-images.githubusercontent.com/120198393/209217486-a4e3a48e-f453-4943-abc6-14d66eca021c.jpeg)

## -What's the lowest 25th percentile salary for people that graduated vs the lowest 25th perecentile salary for people that didn't graduate?

SELECT MIN(Grad_P25) AS Lowest_grad_salary, MIN(Nongrad_P25) AS lowest_nongrad_salary
FROM `college-majors.Grad_Students.Grad students`

RESULTS: ![image](https://user-images.githubusercontent.com/120198393/209220651-14723498-fa32-429c-a561-d7188ae0794b.jpeg)

