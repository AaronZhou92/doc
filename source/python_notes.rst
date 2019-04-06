Python 
======================

1.1 Pandas
---------------------

1. Select the same values between df1 and df2, for the nonidentical values, return NaN. df1 and df2 must be same shape
::
 
    df1.where(df1.values==df2.values)

2. Reading csv contains Chinese character, using encoding:
::

    pd.read_csv(file_path, encoding=''GBK) # GBK us simplified Chinese encoding.

3. Convert column of str to datetime type
%m and %M is different.
::

    pd.to_datetime(date_str_columns, format='%Y%m%d%h%M%s')


4. Convert column names values to first row 
::

    # convert columns names to a new DataFrame
    df_column_names = pd.DataFrame({ii: ii for ii in df_2018.columns.values}, [0]) 
    pd.concat([df_column_names, df_2018], axis=0)

5. Add a fixed hours to datetime index
::

    df.index + pd.Timedelta(hours=8)

6. Sort rows based on single column
::

    df.sort_values(by='col')


1.2 Glob
---------------------

1. Select files with file name sharing same starting letters from given directory
::

    import glob
    selected_file_list = glob.glob(file_path+'\\'+shared_name+'*')


1.3 OS
---------------------

1. list name of files in a given directory
::

    from os import listdir 
    listdir(directory_path)

1.4 Python in Windows
---------------------

1. Double backward slash in file path 
::

    "C:\\Users\\ZHOU XIN\\"
 

1.5 Jupyter notebook
---------------------

1.6 Git
--------------------

1. Pull repo from git
::

    git clone git@github.com:AaronZhou92/doc
    git clone https://github.com/AaronZhou92/doc
	

2. Push local changes to repo
::

    git add .
    git commit -m 'some'
    git push


1.7 ReadtheDocs
---------------------

1. Solution to 'This page does not exist yet'
::

    The name of 'master_doc' inside config.py should be index instead of other names

2. Build the project
::

    Go to folder contains 'make.bat'. 'make html'


1.8 Errors
---------------------

1. ValueError: If using all scalar values, you must pass an index
::

    df = pd.DataFrame({'A': [a], 'B': [b]})
    df = 
    A  B
    0  2  3

or use scalar values and pass an index:
::

    df = pd.DataFrame({'A': a, 'B': b}, index=[0])
    df
    A  B
    0  2  3
    
1.9 Plot
-------------------

1. Figure with two y axis
::

    df.USDCNH.plot()
    ax = df.SH_index.plot(secondary_y=True)
    ax.set_ylabel('SH_index')
    plt.legend()

1.10 Parse web data 
-------------------

1. General method:
::

    import requests
    from bs4 import BeautifulSoup
    url = ''
    response = requests.get(url)
    soup = BeautifulSoup(response.text, 'lxml)

1.11 Programming mistakes
-------------------

1. Date adding 
::

    "from": date(year, month, day),
     "to": date(year, month, day+1)
This is not right because it ignores the month end, 01-31+1, 01-32?
Should using this 
::

    date(2019, 1, 31) + timedelta(days=1)


2. Every time get a new df, take a look at head and tail to see if it is what you want
::

    df_2018 df_2019























