## Diary

### Binary file parser
https://github.com/googlecreativelab/quickdraw-dataset/blob/master/examples/binary_file_parser.py

### String as sequence of octets
>Bytes literals are always prefixed with 'b' or 'B'; they produce an instance of the bytes type instead of the str type. They may only contain ASCII characters; bytes with a numeric value of 128 or greater must be expressed with escapes.

***Solution***
```python
.str.decode("utf-8")
```

https://stackoverflow.com/questions/6269765/what-does-the-b-character-do-in-front-of-a-string-literal

### Convert unix time to readable date in pandas DataFrame
```python
pd.to_datetime(df['timestamp'], unit='s')
```

### Bulk download on Google Cloud
Was unable to make it work with cURL -K or wget -i but anyway, the correct method is below

***Solution***
Install gsutil via Google Cloud SDK  
https://cloud.google.com/sdk/docs/

```sh
gsutil cp -r gs://project_name/folder/ ~/destination_folder
```
