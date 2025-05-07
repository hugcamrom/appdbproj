# 🎬 MoviesDB Application (`appdbproj`)


![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![MySQL](https://img.shields.io/badge/Database-MySQL-informational.svg)
![Neo4j](https://img.shields.io/badge/GraphDB-Neo4j-blue.svg)
![License](https://img.shields.io/badge/License-GPLv3-blue.svg)
![Status](https://img.shields.io/badge/Status-Final-green.svg)


A Python-based database application integrating **MySQL** and **Neo4j** to manage and explore movie-related data. Developed as part of the **Applied Databases** project, it includes full CLI interaction and relationship querying using both relational and graph models.

---

## 📁 Folder Structure

```
appdbproj/
├── Innovation/
│   └── innovation.docx
├── MySQL-Queries/
│   ├── MySQLQA.txt to MySQLQD.txt
├── Neo4j-Queries/
│   ├── Neo4jQA.txt to Neo4jQD.txt
├── PythonApp/
│   ├── main.py
│   └── main.ipynb
└── README.md
```

---

## 🚀 Application Features

### `main.py` — CLI Menu Options

1. ✅ View Directors & Films  
2. ✅ View Actors by Month of Birth  
3. ✅ Add New Actor  
4. ✅ View Married Actors  
5. ✅ Add Actor Marriage  
6. ✅ View Studios  
7. ✅ **View Actor Count by Country** *(Innovation Feature)*  
x. ❌ Exit Application

### `main.ipynb` — For Interactive Testing  
The same logic as `main.py`, tested in cells for development and debugging.

---

## 💡 Innovation: Option 7

> **View Actor Count by Country**  
Displays a grouped count of actors per country using `GROUP BY` in SQL. This adds analytical value to the app and shows usage of relational joins.

```sql
SELECT CountryName, COUNT(*) AS TotalActors
FROM Actor
JOIN Country ON ActorCountryID = CountryID
GROUP BY CountryName
ORDER BY TotalActors DESC;
```

See `Innovation/innovation.docx` for a full description of extra functionality.

---

## 🧠 Technologies Used

- **Python 3.9+**
- **MySQL** – appdbproj database
- **Neo4j Community Edition** – used for actor relationship modeling
- **Packages**:
  - [`mysql-connector-python`](https://pypi.org/project/mysql-connector-python/)
  - [`neo4j`](https://pypi.org/project/neo4j/)

Install with:

```bash
pip install mysql-connector-python neo4j
```

---

## 📚 References

- [Neo4j Community Edition](https://neo4j.com/download-center/#community)
- [Neo4j Python Driver Docs](https://neo4j.com/docs/api/python-driver/current/)
- [MySQL Documentation](https://dev.mysql.com/doc/)
- [Python `datetime` Module](https://docs.python.org/3/library/datetime.html)
- [Python Official Site](https://www.python.org/)
- [Jupyter Notebook](https://jupyter.org/)
- Files including:
  - `innovation.docx`
  - MySQL and Cypher queries
  - Test results

---

## 👤 Author

**Hugo C. Romero**  
Student at [ATU](https://www.atu.ie/)
 
Course: Applied Databases

