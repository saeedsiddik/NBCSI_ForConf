# NotebookCodeStyle_ForConf
Analysis of Notebook Code Style Issue 

## Notebook Files
**`EMSE_Conf_NB_Code_Style_Analysis.ipynb`** - To replicate the results reported in this paper, execute EMSE_Conf_NB_Code_Style_Analysis.ipynb. It is a notebook file where the markdown cells describe the code sections sequentially. 

**`EMSE_Conf_NB_Pylint_Execution.ipynb`** - This notebook contains the code for Pylint execution. It works on notebook files and generates text files containing code style issues and quality ratings.   

**`EMSE_Conf_NB_Pylint_Sqlite_DB.ipynb`** - This notebook contains database handling code, having all the functions, i.e., connect, create, insert, etc. This notebook has the code to process the Pylint output and insert the information into the database table. 

**`EMSE_Conf_Pylint_NB_Text_Analysis.ipynb`** - This notebook contains the code for renaming the output ipynb file name. 

## Data
We stored the data into a SQLite database. The db file is available in data/ directory. The database consists of the following tables:
```
+-------------------+
|      database     |
+-------------------+
| NBFILES           |
| NBRATINGS         |
| NBISSUES          |
+-------------------+
```
1. **`NBFILES`** — a table that stores the notebook Filename, and its Type (ml or nonml).
2. **`NBRATINGS`**  — a table that stores the notebook Filename and its Rating (INT value ranges 0 to 10).
3. **`NBISSUES`**  — a table that stores the the notebook Filename, Issue (Pylint issue code), Cell Number (the code cell containing the issue), and Line (line number containing the issue).
```
+-------------------+	
|      NBFILES     |	
+-------------------+	
| Filename          |	
| Type              |	
+-------------------+	
```
```
+-------------------+	
|      NBRATINGS     |	
+-------------------+	
| Filename          |	
| Rating              |	
+-------------------+	
```
```
+-------------------+	
|      NBISSUES     |	
+-------------------+	
| Filename          |	
| Issue             |	
| CellNo            |	
| Line              |	
+-------------------+	
```
