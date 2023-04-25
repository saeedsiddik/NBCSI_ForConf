# NotebookCodeStyle_ForConf
Analysis of Notebook Code Style Issue 

Execute EMSE_Conf_NB_Code_Style_Analysis.ipynb to get replicate the results reported in this paper. It is a notebook file where the markdown cells describe the code sections sequentially. 

## Data
We stored the data into a SQLite database. The database consists of the following tables:
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
