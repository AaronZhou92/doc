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
::
    pd.to_datetime(date_str_columns, format='%Y%m%d%h%M%s')
%m and %M is different


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

1. Push local changes to repo
::
    git add .
    git commit -, 'some'
    git push