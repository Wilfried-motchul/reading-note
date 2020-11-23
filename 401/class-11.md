# Data Analysis
## JupyterLab Releases
Since JupyterLab 0.32 (February 2018), the releases of JupyterLab are suitable for general daily use by both Jupyter novices and users experienced with the Classic Notebook interface. As of the 1.0 release (June 2019), it is additionally ready for extension writers who wish to further customize the JupyterLab experience for others. Please review the JupyterLab Changelog for detailed descriptions of each release.

The extension developer API is evolving, and we also are currently iterating on UI/UX improvements. We appreciate feedback on our GitHub issues page as we evolve towards a stable extension development API.

JupyterLab will eventually replace the classic Jupyter Notebook. Throughout this transition, the same notebook document format will be supported by both the classic Notebook and JupyterLab.

## Lists Of Lists for CSV Data
Before using NumPy, we’ll first try to work with the data using Python and the csv package. We can read in the file using the csv.reader object, which will allow us to read in and split up all the content from the ssv file.

In the below code, we:

* Import the csv library.
* Open `the winequality-red.csv` file
  * With the file open, create a new `csv.reader` object.
    * Pass in the keyword argument `delimiter=";"` to make sure that the records are split up on the semicolon character instead of the default comma character.

  * Call the list type to get all the rows from the file.
  * Assign the result to `wines`.
```  
import csv
with open('winequality-red.csv', 'r') as f:
    wines = list(csv.reader(f, delimiter=';'))
```
Once we’ve read in the data, we can print out the first 3 rows:
```
print(wines[:3])
```
```
[['fixed acidity', 'volatile acidity', 'citric acid', 'residual sugar', 'chlorides', 'free sulfur dioxide', 'total sulfur dioxide', 'density', 'pH', 'sulphates', 'alcohol', 'quality'], ['7.4', '0.7', '0', '1.9', '0.076', '11', '34', '0.9978', '3.51', '0.56', '9.4', '5'], ['7.8', '0.88', '0', '2.6', '0.098', '25', '67', '0.9968', '3.2', '0.68', '9.8', '5']]
```
The data has been read into a list of lists. Each inner list is a row from the ssv file. As you may have noticed, each item in the entire list of lists is represented as a string, which will make it harder to do computations.

