<H3>Name: Arunkumar S</H3>
<H3>Reg no: 212224230024</H3>
<H3>EX. NO.1</H3>
<H3>DATE</H3>
<H1 ALIGN =CENTER> Introduction to Kaggle and Data preprocessing</H1>

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

**Kaggle :**
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

**Data Preprocessing:**

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

**Need of Data Preprocessing :**

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
STEP 1:Importing the libraries<BR>
STEP 2:Importing the dataset<BR>
STEP 3:Taking care of missing data<BR>
STEP 4:Encoding categorical data<BR>
STEP 5:Normalizing the data<BR>
STEP 6:Splitting the data into test and train<BR>

##  PROGRAM:
```
from sklearn.preprocessing import StandardScaler
from sklearn.model_selection import train_test_split

df = pd.read_csv("/content/Sales-Export_2019-2020.csv")
df

df.isnull().sum()

df = df.fillna(0)
df.isnull().sum()

df.duplicated().sum()

df.info()

numeric_cols = df.select_dtypes(include=['int64', 'float64']).columns
scaler = StandardScaler()
df[numeric_cols] = scaler.fit_transform(df[numeric_cols])
df.head()

X = df.iloc[:, :-1]
Y = df.iloc[:, -1]
print("X Values")
print(X)
print("Y Values")
print(Y)

X_train, X_test, Y_train, Y_test = train_test_split(
    X, Y, test_size=0.2, random_state=42
)
print("X Training Data")
print(X_train)
print("X Testing Data")
print(X_test)
print("Y Training Data")
print(Y_train)
print("Y Testing Data")
print(Y_test)
```


## OUTPUT:
DATASET:

<img width="1742" height="518" alt="image" src="https://github.com/user-attachments/assets/0ef06341-a147-4c30-b2d5-69c785ec9dde" />


NULL VALUES:

<img width="336" height="686" alt="image" src="https://github.com/user-attachments/assets/b3668117-74f8-47e1-a302-d85aa30bca9b" />

<img width="543" height="524" alt="image" src="https://github.com/user-attachments/assets/dacf346f-591d-4603-a0c1-d953c81f3b2d" />


NORMALISED DATA:

<img width="1714" height="395" alt="image" src="https://github.com/user-attachments/assets/e36b9766-2ad2-4546-8320-13b5b8ccf11e" />


DATA SPLITTING: 
x-VALUES
 
<img width="906" height="577" alt="image" src="https://github.com/user-attachments/assets/e3264d0d-92ff-4255-87bb-9ffb27d01776" />


Y-VALUES

<img width="639" height="290" alt="image" src="https://github.com/user-attachments/assets/aa01a6c6-c77d-4546-b8d8-c9e2ef5439bb" />


TRAIN AND TEST DATA:

X-TRAIN

<img width="843" height="577" alt="image" src="https://github.com/user-attachments/assets/fecf0d36-9348-473c-8ec5-d14205f43801" />



X-TEST

<img width="861" height="598" alt="image" src="https://github.com/user-attachments/assets/7873558e-454e-401b-9e20-f5f375024082" />


Y-TRAIN

<img width="537" height="311" alt="image" src="https://github.com/user-attachments/assets/9e8e641a-72bd-4d75-9f53-7499e1fb7a47" />


Y-TEST

<img width="578" height="289" alt="image" src="https://github.com/user-attachments/assets/72423597-4ca4-4100-8849-ea8137742e67" />



## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


