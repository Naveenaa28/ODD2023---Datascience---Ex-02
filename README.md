# Ex02-Outlier
## AIM:
To read a given dataset and remove outliers and save a new dataframe.
## ALGORITHM:
(1) Remove outliers using IQR

(2) After removing outliers in step 1, you get a new dataframe.

(3) use zscore of 3 to remove outliers. This is quite similar to IQR and you will get exact same result

(4) for the data set height_weight.csv find the following

(i) Using IQR detect weight outliers and print them

(ii) Using IQR, detect height outliers and print them
## PROGRAM
```
import pandas as pd
import numpy as np
import seaborn as sns
import pandas as pd
from scipy import stats
df = pd.read_csv("/content/heights.csv")
sns.boxplot(data=df)
sns.scatterplot(data=df)
max =df['height'].quantile(0.90)
min =df['height'].quantile(0.15)
max
min
dq = df[((df['height']>=min)&(df['height']<=max))]
dq
low = min-1.5*iqr
high = max+1.5*iqr
dq = df[((df['height']>=min)&(df['height']<=max))]
dq
```
## ZSCORE:
```
import pandas as pd
import numpy as np
import seaborn as sns
import pandas as pd
from scipy import stats
data = {'weight':[12,15,18,21,24,27,30,33,36,39,42,45,48,51,54,57,60,63,66,69,202,72,75,78,81,84,232,87,90,93,96,99,258]}
df = pd.DataFrame(data)
df
sns.boxplot(data=df)
z = np.abs(stats.zscore(df))
print(df[z['weight']>3])
val =[12,15,18,21,24,27,30,33,36,39,42,45,48,51,54,57,60,63,66,69,202,72,75,78,81,84,232,87,90,93,96,99,258]
out=[]
def d_o(val):
ts=3
m=np.mean(val)
sd=np.std(val)
for i in val:
z=(i-m)/sd
if np.abs(z)>ts:
out.append(i)
return out
op = d_o(val)
op
```
## OUTPUT:
![image](https://github.com/Naveenaa28/ODD2023---Datascience---Ex-02/assets/131433133/435f044e-94c9-48d2-971e-53052683560d)
![image](https://github.com/Naveenaa28/ODD2023---Datascience---Ex-02/assets/131433133/0ec2b1ed-88b0-471c-81e6-2e3fe4287a59)

![image](https://github.com/Naveenaa28/ODD2023---Datascience---Ex-02/assets/131433133/249a7150-536d-4bfa-abe9-c57aa1fe3b32)

![image](https://github.com/Naveenaa28/ODD2023---Datascience---Ex-02/assets/131433133/45015133-a0c7-4154-bd64-5b969db7f72e)

![image](https://github.com/Naveenaa28/ODD2023---Datascience---Ex-02/assets/131433133/6d944d59-2b2c-4153-9047-40afe41fcf95)

![image](https://github.com/Naveenaa28/ODD2023---Datascience---Ex-02/assets/131433133/7db61a85-70ee-4619-bd76-2688be29bfda)

![image](https://github.com/Naveenaa28/ODD2023---Datascience---Ex-02/assets/131433133/1261cf09-cb58-4b2f-a6cd-7ca5f7f746a8)

![image](https://github.com/Naveenaa28/ODD2023---Datascience---Ex-02/assets/131433133/87623320-45d1-45df-b46f-4493afdf3eb2)

![image](https://github.com/Naveenaa28/ODD2023---Datascience---Ex-02/assets/131433133/8768ba05-ae9d-418a-a5f9-b21fff838845)
## RESULT:
Thus, the given data is read,remove outliers and save a new dataframe was created and executed successfully.











