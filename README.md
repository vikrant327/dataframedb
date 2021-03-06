# dataframedb
Dataframe to SQL database table. Tool was orginally configured to work with PostgreSQL, and later added configuration for MS Sql Server

# Installation
pip install git+https://github.com/vikrant327/dataframedb

# on Jupyter Notebook
!pip install git+https://github.com/vikrant327/dataframedb


# Usage
```sh
from dataframedb.PGSqlAlchemy import PGSqlAlchemy

# initialize configuration
config_db = {
  'serverType':'SqlServer',   # other valid value is 'pg'
  'server' : '0.0.0.0',   # DB server ip
  'tablename': 'table_name',   # Table name to work with, appending records or creating a new one
  'port': database_port,  # Database Port number
  'dbname':'database_name',  # Database name
  'schema':'public',   # database schema
  'username':'username',  # database username
  'password':'password',   # database password
  'dataframe':df_name,  # pnadas dataframe to insert to database
  'mode':'replace'   # 'replace' if replacing existing table or creating new, 'append' if appending records to existing table
}

df_sql = PGSqlAlchemy(config_db)
db_response = df_sql.syncDatabase()
print(db_response)

```

