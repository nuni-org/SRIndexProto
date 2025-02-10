# SRIndexProto
Prototype of calculator for Social Relationship Index
- It is designed to quantify the investments in your social relationship
- You can estimate the Social Relationship Index by calculating the average of individual index for each person(=case).
- The range of this index is 0 to 100.

BUT, PLEASE DO NOT BE SERIOUS.

## Steps for index calculation

The Social Relationship Index is "Weighted Sum" of two parameters: Importance and Performance.

Your social relationship investments are categorized into three elements: Money, Time, and Emotion.

### Importance
Please rate importance of three elements on a 5-point scale, based on your personal values.

Weights of importance are calculated as follows(%):
- (importance of one element / total) * 100
- total: summation of three importances points
  
### Performance
To calculate the performance, you need data of arguments in the three elements as follows:
- Money: give-and-take between each other
- Time: meetings spent together
- Emotion: contact exchanged with each other

These are measured on a 5-point scale, based on your relative investment ratio.

### Index
Individual index for each person(=case):
- index of element 1 + index of element 2 + index of element 3 
- (Importance weight * Perfomance point) of element 1 + (Importance weight * Perfomance point) of element 2 + (Importance weight * Perfomance point) of element 3

Social Relationship Index:
- (index case 1 + index case 2 + ... index case n) / n 
- (the summation of all individual index for each person) / (the number of persons of you evaluated) 

# Use
```bash
First, enter the following console command:

$ srindex

and you will input the arguments into the function in several steps.

Please read the script and think of people around you carefully.
Please answer the questions faithfully.


Results are shown as follows:

--------------------------------- RESULT ----------------------------------------
The importance of each elements you answered: scale of 100
- money: 38.46
- time: 30.77
- emotion: 30.77

The average performance of each elements you answered: scale of 100
- money: 70.00
- time: 55.00
- emotion: 75.00
*The criteria for converting to a score out of 100 are as follows:
point1: 0 | point2: 25 | point3: 50 | point4: 75 | point5: 100

The table of 'Performance' for each case of each element is as follows:
┏━━━━━━━━━┳━━━━━━━┳━━━━━━┳━━━━━━━━━┓
┃ Case ID ┃ Money ┃ Time ┃ Emotion ┃
┡━━━━━━━━━╇━━━━━━━╇━━━━━━╇━━━━━━━━━┩
│ Average │  70.0 │ 55.0 │    75.0 │
│    1    │  75.0 │ 50.0 │    75.0 │
│    2    │  25.0 │ 75.0 │    50.0 │
│    3    │  75.0 │ 50.0 │    75.0 │
│    4    │ 100.0 │ 75.0 │   100.0 │
│    5    │  75.0 │ 25.0 │    75.0 │
└─────────┴───────┴──────┴─────────┘

Totally, the Social Relationship Index is: 66.92

The table of 'Index'(=Importance*Performance) by case is as follows:
┏━━━━━━━━━┳━━━━━━━┳━━━━━━━┳━━━━━━━━━┳━━━━━━━━━━━━━━━━━━━━━━━━━━━┓
┃ Case ID ┃ Money ┃ Time  ┃ Emotion ┃ Social Relationship Index ┃
┡━━━━━━━━━╇━━━━━━━╇━━━━━━━╇━━━━━━━━━╇━━━━━━━━━━━━━━━━━━━━━━━━━━━┩
│ Average │ 26.92 │ 16.92 │  23.08  │           66.92           │
│    1    │ 28.85 │ 15.38 │  23.08  │           67.31           │
│    2    │ 9.62  │ 23.08 │  15.38  │           48.08           │
│    3    │ 28.85 │ 15.38 │  23.08  │           67.31           │
│    4    │ 38.46 │ 23.08 │  30.77  │           92.31           │
│    5    │ 28.85 │ 7.69  │  23.08  │           59.62           │
└─────────┴───────┴───────┴─────────┴───────────────────────────┘
---------------------------------------------------------------------------------

```


 
In order to produce the Social Relationship Index,
please read carefully the Introduction of index and the criteria for evaluating.   


# Development environment setting guide
```bash
# install PDM
# git clone ...
# pdm venv create
$ source .venv/bin/activate
$ pdm install
# $ vi ...

$ git add <FILE_NAME>
$ git commit -a
$ git push
$ pdm publish --username __token__ --password $PYPI_TOKEN

View at:
https://pypi.org/project/SRIndexProto/

# PR - Merge
# Tag - Releases
```

## Enhancement plans
IPA (Importance-Perfomance Analysis): 
- A quantitative approach for measuring how people feel about certain characteristics of an issue or a thing (Martilla & James, 1977)
- Chart: Importance-Performance Matrix
![image](https://github.com/user-attachments/assets/595edffe-f813-446f-91c3-e3948f9a1514)




### Ref
- https://pdm-project.org/en/latest/
- https://packaging.python.org/en/latest/tutorials/packaging-projects/
- [console_scripts](https://packaging.python.org/en/latest/specifications/entry-points/#entry-points-specification)

