# CS27020 Lecture 8
__Wednesay, October 18th 2017__  
Lecture: ara11@aber.ac.uk   
Notes: ela12@aber.ac.uk

## Functional Dependencies and 2nd Normal Form

### Functional Dependencies:

X &rightarrow; Y

- Y functionally depends on X
- From X we can determine Y (i.e. X is a determinant)

#### Example:
- `login` &rightarrow; `name`
- `name` is functionally dependent on `login`
- You can determine the name of the staff from `login`
- `login` determines `name`
- `login` is called the determinant