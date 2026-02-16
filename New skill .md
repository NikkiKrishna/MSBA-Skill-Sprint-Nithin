```python
import pandas as pd
df = pd.read_csv('customer_shopping_behavior.csv')
```


```python
df.head()
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Customer ID</th>
      <th>Age</th>
      <th>Gender</th>
      <th>Item Purchased</th>
      <th>Category</th>
      <th>Purchase Amount (USD)</th>
      <th>Location</th>
      <th>Size</th>
      <th>Color</th>
      <th>Season</th>
      <th>Review Rating</th>
      <th>Subscription Status</th>
      <th>Shipping Type</th>
      <th>Discount Applied</th>
      <th>Promo Code Used</th>
      <th>Previous Purchases</th>
      <th>Payment Method</th>
      <th>Frequency of Purchases</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>55</td>
      <td>Male</td>
      <td>Blouse</td>
      <td>Clothing</td>
      <td>53</td>
      <td>Kentucky</td>
      <td>L</td>
      <td>Gray</td>
      <td>Winter</td>
      <td>3.1</td>
      <td>Yes</td>
      <td>Express</td>
      <td>Yes</td>
      <td>Yes</td>
      <td>14</td>
      <td>Venmo</td>
      <td>Fortnightly</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>19</td>
      <td>Male</td>
      <td>Sweater</td>
      <td>Clothing</td>
      <td>64</td>
      <td>Maine</td>
      <td>L</td>
      <td>Maroon</td>
      <td>Winter</td>
      <td>3.1</td>
      <td>Yes</td>
      <td>Express</td>
      <td>Yes</td>
      <td>Yes</td>
      <td>2</td>
      <td>Cash</td>
      <td>Fortnightly</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>50</td>
      <td>Male</td>
      <td>Jeans</td>
      <td>Clothing</td>
      <td>73</td>
      <td>Massachusetts</td>
      <td>S</td>
      <td>Maroon</td>
      <td>Spring</td>
      <td>3.1</td>
      <td>Yes</td>
      <td>Free Shipping</td>
      <td>Yes</td>
      <td>Yes</td>
      <td>23</td>
      <td>Credit Card</td>
      <td>Weekly</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>21</td>
      <td>Male</td>
      <td>Sandals</td>
      <td>Footwear</td>
      <td>90</td>
      <td>Rhode Island</td>
      <td>M</td>
      <td>Maroon</td>
      <td>Spring</td>
      <td>3.5</td>
      <td>Yes</td>
      <td>Next Day Air</td>
      <td>Yes</td>
      <td>Yes</td>
      <td>49</td>
      <td>PayPal</td>
      <td>Weekly</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>45</td>
      <td>Male</td>
      <td>Blouse</td>
      <td>Clothing</td>
      <td>49</td>
      <td>Oregon</td>
      <td>M</td>
      <td>Turquoise</td>
      <td>Spring</td>
      <td>2.7</td>
      <td>Yes</td>
      <td>Free Shipping</td>
      <td>Yes</td>
      <td>Yes</td>
      <td>31</td>
      <td>PayPal</td>
      <td>Annually</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.info
```




    <bound method DataFrame.info of       Customer ID  Age  Gender Item Purchased     Category  \
    0               1   55    Male         Blouse     Clothing   
    1               2   19    Male        Sweater     Clothing   
    2               3   50    Male          Jeans     Clothing   
    3               4   21    Male        Sandals     Footwear   
    4               5   45    Male         Blouse     Clothing   
    ...           ...  ...     ...            ...          ...   
    3895         3896   40  Female         Hoodie     Clothing   
    3896         3897   52  Female       Backpack  Accessories   
    3897         3898   46  Female           Belt  Accessories   
    3898         3899   44  Female          Shoes     Footwear   
    3899         3900   52  Female        Handbag  Accessories   
    
          Purchase Amount (USD)       Location Size      Color  Season  \
    0                        53       Kentucky    L       Gray  Winter   
    1                        64          Maine    L     Maroon  Winter   
    2                        73  Massachusetts    S     Maroon  Spring   
    3                        90   Rhode Island    M     Maroon  Spring   
    4                        49         Oregon    M  Turquoise  Spring   
    ...                     ...            ...  ...        ...     ...   
    3895                     28       Virginia    L  Turquoise  Summer   
    3896                     49           Iowa    L      White  Spring   
    3897                     33     New Jersey    L      Green  Spring   
    3898                     77      Minnesota    S      Brown  Summer   
    3899                     81     California    M      Beige  Spring   
    
          Review Rating Subscription Status   Shipping Type Discount Applied  \
    0               3.1                 Yes         Express              Yes   
    1               3.1                 Yes         Express              Yes   
    2               3.1                 Yes   Free Shipping              Yes   
    3               3.5                 Yes    Next Day Air              Yes   
    4               2.7                 Yes   Free Shipping              Yes   
    ...             ...                 ...             ...              ...   
    3895            4.2                  No  2-Day Shipping               No   
    3896            4.5                  No    Store Pickup               No   
    3897            2.9                  No        Standard               No   
    3898            3.8                  No         Express               No   
    3899            3.1                  No    Store Pickup               No   
    
         Promo Code Used  Previous Purchases Payment Method Frequency of Purchases  
    0                Yes                  14          Venmo            Fortnightly  
    1                Yes                   2           Cash            Fortnightly  
    2                Yes                  23    Credit Card                 Weekly  
    3                Yes                  49         PayPal                 Weekly  
    4                Yes                  31         PayPal               Annually  
    ...              ...                 ...            ...                    ...  
    3895              No                  32          Venmo                 Weekly  
    3896              No                  41  Bank Transfer              Bi-Weekly  
    3897              No                  24          Venmo              Quarterly  
    3898              No                  24          Venmo                 Weekly  
    3899              No                  33          Venmo              Quarterly  
    
    [3900 rows x 18 columns]>




```python
df.describe(include='all')
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Customer ID</th>
      <th>Age</th>
      <th>Gender</th>
      <th>Item Purchased</th>
      <th>Category</th>
      <th>Purchase Amount (USD)</th>
      <th>Location</th>
      <th>Size</th>
      <th>Color</th>
      <th>Season</th>
      <th>Review Rating</th>
      <th>Subscription Status</th>
      <th>Shipping Type</th>
      <th>Discount Applied</th>
      <th>Promo Code Used</th>
      <th>Previous Purchases</th>
      <th>Payment Method</th>
      <th>Frequency of Purchases</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>3900.000000</td>
      <td>3900.000000</td>
      <td>3900</td>
      <td>3900</td>
      <td>3900</td>
      <td>3900.000000</td>
      <td>3900</td>
      <td>3900</td>
      <td>3900</td>
      <td>3900</td>
      <td>3863.000000</td>
      <td>3900</td>
      <td>3900</td>
      <td>3900</td>
      <td>3900</td>
      <td>3900.000000</td>
      <td>3900</td>
      <td>3900</td>
    </tr>
    <tr>
      <th>unique</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>2</td>
      <td>25</td>
      <td>4</td>
      <td>NaN</td>
      <td>50</td>
      <td>4</td>
      <td>25</td>
      <td>4</td>
      <td>NaN</td>
      <td>2</td>
      <td>6</td>
      <td>2</td>
      <td>2</td>
      <td>NaN</td>
      <td>6</td>
      <td>7</td>
    </tr>
    <tr>
      <th>top</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>Male</td>
      <td>Blouse</td>
      <td>Clothing</td>
      <td>NaN</td>
      <td>Montana</td>
      <td>M</td>
      <td>Olive</td>
      <td>Spring</td>
      <td>NaN</td>
      <td>No</td>
      <td>Free Shipping</td>
      <td>No</td>
      <td>No</td>
      <td>NaN</td>
      <td>PayPal</td>
      <td>Every 3 Months</td>
    </tr>
    <tr>
      <th>freq</th>
      <td>NaN</td>
      <td>NaN</td>
      <td>2652</td>
      <td>171</td>
      <td>1737</td>
      <td>NaN</td>
      <td>96</td>
      <td>1755</td>
      <td>177</td>
      <td>999</td>
      <td>NaN</td>
      <td>2847</td>
      <td>675</td>
      <td>2223</td>
      <td>2223</td>
      <td>NaN</td>
      <td>677</td>
      <td>584</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>1950.500000</td>
      <td>44.068462</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>59.764359</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>3.750065</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>25.351538</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>std</th>
      <td>1125.977353</td>
      <td>15.207589</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>23.685392</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>0.716983</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>14.447125</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1.000000</td>
      <td>18.000000</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>20.000000</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>2.500000</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>1.000000</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>975.750000</td>
      <td>31.000000</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>39.000000</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>3.100000</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>13.000000</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>1950.500000</td>
      <td>44.000000</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>60.000000</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>3.800000</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>25.000000</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>2925.250000</td>
      <td>57.000000</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>81.000000</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>4.400000</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>38.000000</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
    <tr>
      <th>max</th>
      <td>3900.000000</td>
      <td>70.000000</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>100.000000</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>5.000000</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>50.000000</td>
      <td>NaN</td>
      <td>NaN</td>
    </tr>
  </tbody>
</table>
</div>




```python
df.isnull().sum()
```




    Customer ID                0
    Age                        0
    Gender                     0
    Item Purchased             0
    Category                   0
    Purchase Amount (USD)      0
    Location                   0
    Size                       0
    Color                      0
    Season                     0
    Review Rating             37
    Subscription Status        0
    Shipping Type              0
    Discount Applied           0
    Promo Code Used            0
    Previous Purchases         0
    Payment Method             0
    Frequency of Purchases     0
    dtype: int64




```python
df['Review Rating'] = df.groupby('Category')['Review Rating'].transform(lambda x: x.fillna(x.median()))
```


```python
df.isnull().sum()
```




    Customer ID               0
    Age                       0
    Gender                    0
    Item Purchased            0
    Category                  0
    Purchase Amount (USD)     0
    Location                  0
    Size                      0
    Color                     0
    Season                    0
    Review Rating             0
    Subscription Status       0
    Shipping Type             0
    Discount Applied          0
    Promo Code Used           0
    Previous Purchases        0
    Payment Method            0
    Frequency of Purchases    0
    dtype: int64




```python
df.columns = df.columns.str.lower()
df.columns = df.columns.str.replace(' ','_')
df = df.rename(columns={'purchase_amount_(usd)':'purchase_amount'})
```


```python
df.columns
```




    Index(['customer_id', 'age', 'gender', 'item_purchased', 'category',
           'purchase_amount', 'location', 'size', 'color', 'season',
           'review_rating', 'subscription_status', 'shipping_type',
           'discount_applied', 'promo_code_used', 'previous_purchases',
           'payment_method', 'frequency_of_purchases'],
          dtype='object')




```python
labels = ['Young Adult', 'Adult', 'Middle-aged', 'Senior']
df['age_group'] = pd.qcut(df['age'], q=4, labels = labels)
```


```python
df[['age','age_group']].head(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>age</th>
      <th>age_group</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>55</td>
      <td>Middle-aged</td>
    </tr>
    <tr>
      <th>1</th>
      <td>19</td>
      <td>Young Adult</td>
    </tr>
    <tr>
      <th>2</th>
      <td>50</td>
      <td>Middle-aged</td>
    </tr>
    <tr>
      <th>3</th>
      <td>21</td>
      <td>Young Adult</td>
    </tr>
    <tr>
      <th>4</th>
      <td>45</td>
      <td>Middle-aged</td>
    </tr>
    <tr>
      <th>5</th>
      <td>46</td>
      <td>Middle-aged</td>
    </tr>
    <tr>
      <th>6</th>
      <td>63</td>
      <td>Senior</td>
    </tr>
    <tr>
      <th>7</th>
      <td>27</td>
      <td>Young Adult</td>
    </tr>
    <tr>
      <th>8</th>
      <td>26</td>
      <td>Young Adult</td>
    </tr>
    <tr>
      <th>9</th>
      <td>57</td>
      <td>Middle-aged</td>
    </tr>
  </tbody>
</table>
</div>




```python
frequency_mapping = {
    'Fortnightly': 14,
    'Weekly': 7,
    'Monthly': 30,
    'Quarterly': 90,
    'Bi-Weekly': 14,
    'Annually': 365,
    'Every 3 Months': 90
}

df['purchase_frequency_days'] = df['frequency_of_purchases'].map(frequency_mapping)
```


```python
df[['purchase_frequency_days','frequency_of_purchases']].head(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>purchase_frequency_days</th>
      <th>frequency_of_purchases</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>14</td>
      <td>Fortnightly</td>
    </tr>
    <tr>
      <th>1</th>
      <td>14</td>
      <td>Fortnightly</td>
    </tr>
    <tr>
      <th>2</th>
      <td>7</td>
      <td>Weekly</td>
    </tr>
    <tr>
      <th>3</th>
      <td>7</td>
      <td>Weekly</td>
    </tr>
    <tr>
      <th>4</th>
      <td>365</td>
      <td>Annually</td>
    </tr>
    <tr>
      <th>5</th>
      <td>7</td>
      <td>Weekly</td>
    </tr>
    <tr>
      <th>6</th>
      <td>90</td>
      <td>Quarterly</td>
    </tr>
    <tr>
      <th>7</th>
      <td>7</td>
      <td>Weekly</td>
    </tr>
    <tr>
      <th>8</th>
      <td>365</td>
      <td>Annually</td>
    </tr>
    <tr>
      <th>9</th>
      <td>90</td>
      <td>Quarterly</td>
    </tr>
  </tbody>
</table>
</div>




```python
df[['discount_applied','promo_code_used']].head(10)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>discount_applied</th>
      <th>promo_code_used</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Yes</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Yes</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Yes</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Yes</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Yes</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Yes</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Yes</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Yes</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>8</th>
      <td>Yes</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Yes</td>
      <td>Yes</td>
    </tr>
  </tbody>
</table>
</div>




```python
(df['discount_applied'] == df['promo_code_used']).all()
```




    np.True_




```python
df = df.drop('promo_code_used', axis=1)
```


```python
df.columns
```




    Index(['customer_id', 'age', 'gender', 'item_purchased', 'category',
           'purchase_amount', 'location', 'size', 'color', 'season',
           'review_rating', 'subscription_status', 'shipping_type',
           'discount_applied', 'previous_purchases', 'payment_method',
           'frequency_of_purchases', 'age_group', 'purchase_frequency_days'],
          dtype='object')




```python
!pip install psycopg2-binary sqlalchemy
```

    Collecting psycopg2-binary
      Downloading psycopg2_binary-2.9.11-cp313-cp313-macosx_11_0_arm64.whl.metadata (4.9 kB)
    Requirement already satisfied: sqlalchemy in /opt/anaconda3/lib/python3.13/site-packages (2.0.39)
    Requirement already satisfied: typing-extensions>=4.6.0 in /opt/anaconda3/lib/python3.13/site-packages (from sqlalchemy) (4.12.2)
    Downloading psycopg2_binary-2.9.11-cp313-cp313-macosx_11_0_arm64.whl (3.9 MB)
    [2K   [38;2;114;156;31m━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━[0m [32m3.9/3.9 MB[0m [31m880.4 kB/s[0m eta [36m0:00:00[0m1m891.3 kB/s[0m eta [36m0:00:01[0m
    Installing collected packages: psycopg2-binary
    Successfully installed psycopg2-binary-2.9.11



```python
from sqlalchemy import create_engine

# Step 1: Connect to PostgreSQL
# Replace placeholders with your actual details
username = "postgres"      # default user
password = "Krishna221#" # the password you set during installation
host = "localhost"         # if running locally
port = "5432"              # default PostgreSQL port
database = "customer_behavior"    # the database you created in pgAdmin

engine = create_engine(f"postgresql+psycopg2://{username}:{password}@{host}:{port}/{database}")

# Step 2: Load DataFrame into PostgreSQL
table_name = "customer"   # choose any table name
df.to_sql(table_name, engine, if_exists="replace", index=False)

print(f"Data successfully loaded into table '{table_name}' in database '{database}'.")
```

    Data successfully loaded into table 'customer' in database 'customer_behavior'.



```python
!pip install pymysql sqlalchemy
```

    Collecting pymysql
      Downloading pymysql-1.1.2-py3-none-any.whl.metadata (4.3 kB)
    Requirement already satisfied: sqlalchemy in /opt/anaconda3/lib/python3.13/site-packages (2.0.39)
    Requirement already satisfied: typing-extensions>=4.6.0 in /opt/anaconda3/lib/python3.13/site-packages (from sqlalchemy) (4.12.2)
    Downloading pymysql-1.1.2-py3-none-any.whl (45 kB)
    Installing collected packages: pymysql
    Successfully installed pymysql-1.1.2



```python
from sqlalchemy import create_engine
import pandas as pd

# Connection details (Postgres defaults)
username = "postgres"
password = "Krishna221#"
host = "localhost"
port = "5432"
database = "customer_behavior"

# FIX: Changed 'mysql+pymysql' to 'postgresql+psycopg2'
engine = create_engine(f"postgresql+psycopg2://{username}:{password}@{host}:{port}/{database}")

# Write DataFrame to PostgreSQL
table_name = "customer"
df.to_sql(table_name, engine, if_exists="replace", index=False)

# Read back sample
df_sample = pd.read_sql(f"SELECT * FROM {table_name} LIMIT 5;", engine)
print(df_sample)
```

       customer_id  age gender item_purchased  category  purchase_amount  \
    0            1   55   Male         Blouse  Clothing               53   
    1            2   19   Male        Sweater  Clothing               64   
    2            3   50   Male          Jeans  Clothing               73   
    3            4   21   Male        Sandals  Footwear               90   
    4            5   45   Male         Blouse  Clothing               49   
    
            location size      color  season  review_rating subscription_status  \
    0       Kentucky    L       Gray  Winter            3.1                 Yes   
    1          Maine    L     Maroon  Winter            3.1                 Yes   
    2  Massachusetts    S     Maroon  Spring            3.1                 Yes   
    3   Rhode Island    M     Maroon  Spring            3.5                 Yes   
    4         Oregon    M  Turquoise  Spring            2.7                 Yes   
    
       shipping_type discount_applied  previous_purchases payment_method  \
    0        Express              Yes                  14          Venmo   
    1        Express              Yes                   2           Cash   
    2  Free Shipping              Yes                  23    Credit Card   
    3   Next Day Air              Yes                  49         PayPal   
    4  Free Shipping              Yes                  31         PayPal   
    
      frequency_of_purchases    age_group  purchase_frequency_days  
    0            Fortnightly  Middle-aged                       14  
    1            Fortnightly  Young Adult                       14  
    2                 Weekly  Middle-aged                        7  
    3                 Weekly  Young Adult                        7  
    4               Annually  Middle-aged                      365  



```python
from sqlalchemy import create_engine
import urllib.parse  # Import this to handle the # character

username = "postgres"
password = urllib.parse.quote_plus("Krishna221#") # Encodes # to %23
host = "localhost"
port = "5432"
database = "customer_behavior"

# The URL-encoded string is much safer
engine = create_engine(f"postgresql+psycopg2://{username}:{password}@{host}:{port}/{database}")

```


```python

```
