

Training Piscine Python for Data Science - 1 Array 

_Summary: Today, you will discover arrays, their manipulations, and work on images._ 

_Version: 2.0_ 

|**Co**|**ntents**||
|---|---|---|
|**I**|**General rules**|**2**|
|**II**|**Specific instructions of the day**|**3**|
|**III**|**Exercise 00**|**4**|
|**IV**|**Exercise 01**|**5**|
|**V**|**Exercise 02**|**6**|
|**VI**|**Exercise 03**|**7**|
|**VII**|**Exercise 04**|**9**|
|**VIII**|**Exercise 05**|**11**|
|**IX**|**Submission and peer-evaluation**|**14**|



1 

# **Chapter I** 

# **General rules** 

- You have to render your modules from a computer in the cluster or using a virtual machine: 

   - You can choose the operating system to use for your virtual machine 

   - Your virtual machine must have all the necessary software to complete your project. This software must be configured and installed. 

- Or you can use the computer directly if the tools are available. 

   - Make sure you have the space on your session to install what you need for all the modules (use the goinfre if your campus has it) 

   - You must have everything installed before the evaluations 

- We encourage you to create test programs for your project even though this work **won’t have to be submitted and won’t be graded** . It will give you a chance to easily test your work and your peers’ work. You will find those tests especially useful during your defence. Indeed, during defence, you are free to use your tests and/or the tests of the peer you are evaluating. 

- Submit your work to your assigned git repository. Only the work in the git repository will be graded. If Deepthought is assigned to grade your work, it will be done after your peer-evaluations. If an error happens in any section of your work during Deepthought’s grading, the evaluation will stop. 

- You must use Python version 3.10 or higher. 

- Your library imports must be explicit. Wildcard imports such as `from pandas import *` are not allowed and will result in a score of `0` for the exercise. 

- Global variables are not allowed. 

- By Odin, by Thor ! Use your brain !!! 

2 

# **Chapter II** 

# **Specific instructions of the day** 

- No code in the global scope. Use functions! 

- Each program must have its main and not be a simple script: 

```
defmain():
#yourtestsandyourerrorhandling
if__name__=="__main__":
main()
```

- Any exception not caught will invalidate the exercices, even in the event of an error that you were asked to test. 

- You can use any built-in function if it is not prohibited in the exercise. 

- All your functions must have a documentation (__doc__) 

- Your code must be at the norm 

   - pip install flake8 

   - alias norminette=flake8 

3 

# **Chapter III Exercise 00** 

|||Exercis|e 00|
|---|---|---|---|
||Exer|cice 00:|Give my BMI|
|Turn-in directory : _ex_00_/_||||
|Files to turn in : `give_bmi.py`||||
|Allowed functions : `numpy or `|`any `|`lib of `|`table manipulation`|



Your function, give_bmi, takes 2 lists of integers or floats in input and returns a list of BMI values. 

Your function, apply_limit, accepts a list of integers or floats and an integer representing a limit as parameters. It returns a list of booleans (True if above the limit). You have to handle error cases if the lists are not the same size, are not int or float... 

The prototype of functions is: 

```
defgive_bmi(height:list[int|float],weight:list[int|float])->list[int|float]:
#yourcodehere
defapply_limit(bmi:list[int|float],limit:int)->list[bool]:
#yourcodehere
```

Your tester.py: 

```
fromgive_bmiimportgive_bmi,apply_limit
height=[2.71,1.15]
weight=[165.3,38.4]
bmi=give_bmi(height,weight)
print(bmi,type(bmi))
print(apply_limit(bmi,26))
```

Expected output: 

```
$>pythontester.py
[22.507863455018317,29.0359168241966]<class'list'>
[False,True]
$>
```

4 

# **Chapter IV Exercise 01** 

Exercise 01 Exercice 01: 2D array Turn-in directory : _ex_ 01 _<u>/</u>_ Files to turn in : `array2D.py` Allowed functions : `numpy or any lib of table manipulation` 

Write a function that takes as parameters a 2D array, prints its shape, and returns a truncated version of the array based on the provided start and end arguments. You must use the slicing method. 

You have to handle error cases, for example if the input is not a valid 2D array. 

The prototype of function is: 

```
defslice_me(family:list,start:int,end:int)->list:
#yourcodehere
```

Your tester.py: 

```
fromarray2Dimportslice_me
family=[[1.80,78.4],
[2.15,102.7],
[2.10,98.5],
[1.88,75.2]]
print(slice_me(family,0,2))
print(slice_me(family,1,-2))
```

Expected output: 

```
$>pythontest_array2D.py
Myshapeis:(4,2)
Mynewshapeis:(2,2)
[[1.8,78.4],[2.15,102.7]]
Myshapeis:(4,2)
Mynewshapeis:(1,2)
[[2.15,102.7]]
$>
```

5 

# **Chapter V Exercise 02** 

Exercise 02 Exercice 02: load my image Turn-in directory : _ex_ 02 _<u>/</u>_ Files to turn in : `load_image.py` Allowed functions : `all libs for load images and table manipulation` 

You need to write a function that loads an image, prints its format, and its pixels content in RGB format. 

You have to handle, at least, JPG and JPEG format. 

You need to handle any error with a clear error message 

Here’s how it should be prototyped : 

```
defft_load(path:str)->array:(youcanreturnthedesiredformat)
#yourcodehere
```

Your tester.py: 

```
fromload_imageimportft_load
print(ft_load("landscape.jpg"))
```

Expected output: 

```
$>pythontester.py
Theshapeofimageis:(257,450,3)
[[[194283]
[234284]
[284384]
...
[000]
[111]
[111]]]
$>
```

6 

# **Chapter VI Exercise 03** 

Exercise 03 Exercice 03: zoom on me Turn-in directory : _ex_ 03 _<u>/</u>_ Files to turn in : `load_image.py, zoom.py` Allowed functions : `all libs for load, manipulate, display image and table manipulation` 

Create a program that should load the image "animal.jpeg", print some information about it and display it after "zooming". 

- The size in pixel on both X and Y axis 

- The number of channel 

- The pixel content of the image. 

- Display the scale on the x and y axis on the image 

If anything went wrong, the program must not stop abruptly and handle any error with a clear message. 

Expected output: 

```
$>pythonzoom.py
Theshapeofimageis:(768,1024,3)
[[[120111132]
[139130151]
[155146167]
...
[12015694]
[11915490]
[11815389]]]
Newshapeafterslicing:(400,400,1)or(400,400)
[[[167]
[180]
[194]
...
[102]
[104]
[103]]]
$>
```

7 

Array 

Training Piscine Python for Data Science - 1 

Expected output: 



<!-- Start of picture text -->
500 SpeeBRSe- SENG ENhE ed |<br>100 = SS ees<br>SSN vith Yy2<br>150 i YF<br>200 = * =<br>[2g , Bc =|<br>2504 pigs© =<br>300 Ease<br>Ke 7 <<br>350 + }\) —_<br>0 50 100 150 200 250 300 350<br><!-- End of picture text -->



```
Yourarrayafterslicingandthezoomareamaybedifferent.
```

8 

**Chapter VII Exercise 04** Exercise 04 Exercice 04: rotate me Turn-in directory : _ex_ 04 _<u>/</u>_ Files to turn in : `load_image.py, rotate.py` Allowed functions : `all libs for load, manipulate, display image and table` ~~—————~~ `manipulation` Make a program which must load the image "animal.jpeg", cut a square part from it and transpose it to produce the image below. It should display it, print the new shape and the data of the image after the transpose. Expected output: <mark>`$> python rotate.py The shape of image is: (400, 400, 1) or (400, 400) [[[167] [180] [194] ... [102] [104] [103]]] New shape after Transpose: (400, 400) [[167 180 194 ... 64 50 72] ... [115 116 119 ... 102 104 103]] $>`</mark> `Your array after the transpose can be different. You can look for the transpose method, it could help you ...` ~~—~~ 9 

Array 

Training Piscine Python for Data Science - 1 



```
Youhavetodothetransposeyourself,nolibraryisallowedforthe
transpose
```

## Expected output: 



<!-- Start of picture text -->
oO ST Aad<br>Lee Til Ae<br>50 & a Nis \ 4 ‘\ eo ea<br>100 Sow \ \<br>SU “ ¥<br>Sn<br>200 a4 Hei<br>250 ee ieee, > 4 ail<br>a hy Wy<br>350 } LS ae<br>i, mt; NY y<br>oO 50 100 150 200 250 300 350<br><!-- End of picture text -->



<!-- Start of picture text -->
10<br><!-- End of picture text -->

**Chapter VIII Exercise 05** Exercise 05 Exercice 05: Pimp my image Turn-in directory : _ex_ 05 _<u>/</u>_ Files to turn in : `load_image.py,` <u>`pimp_image.py`</u> Allowed functions : `all libs for load, manipulate, display image and table` ~~——~~ `manipulation` You need to develop 5 functions capable of applying a variety of color filters to images, while keeping the image shape the same. Here’s how they should be prototyped : `def ft_invert(array) -> array:` _`#your code here`_ `def ft_red(array) -> array:` _`#your code here`_ `def ft_green(array) -> array:` _`#your code here`_ `def ft_blue(array) -> array:` _`#your code here`_ `def ft_grey(array) -> array:` _`#your code here`_ ~~<mark>a</mark>~~ You have some restriction operators for each function: (you can only use those given, you don’t have to use them all) 

- `invert` : =, +, -, * 

- `red` : =, * 

- `green` : =, - 

- `blue` : = 

- `grey` : =, / 



<!-- Start of picture text -->
11<br><!-- End of picture text -->

Array 

Training Piscine Python for Data Science - 1 

## Your tester.py: 

```
fromload_imageimportft_load
frompimp_imageimportft_invert
...
array=ft_load("landscape.jpg")
ft_invert(array)
ft_red(array)
ft_green(array)
ft_blue(array)
ft_grey(array)
print(ft_invert.__doc__)
```

## Expected output: (docstrings can be different) 

```
$>pythontester.py
Theshapeofimageis:(257,450,3)
[[[194283]
[234284]
[284384]
...
[000]
[111]
[111]]]
...
Invertsthecoloroftheimagereceived.
$>
```

12 

Array 

Training Piscine Python for Data Science - 1 

Expected output: (you must display the images transformed) 







<!-- Start of picture text -->
Figure VIII.1: Original Figure VIII.2: Invert<br>=<br>Figure VIII.3: Red Figure VIII.4: Green<br>a<br>Figure VIII.5: Blue Figure VIII.6: Grey<br>is<br>13<br><!-- End of picture text -->

# **Chapter IX** 

# **Submission and peer-evaluation** 

Turn in your assignment in your `Git` repository as usual. Only the work inside your repository will be evaluated during the defense. Don’t hesitate to double check the names of your folders and files to ensure they are correct. 



```
Theevaluationprocesswillhappenonthecomputeroftheevaluated
group.
```

14 

