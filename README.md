# best-practices

There seems to be many tools and workflows that can be used for data analytics and data science.
The purpose of this file is to document and record some best practices I come across to help with 
organisation of code and workflow, so as to at least have some sort of general structure that will
help with clarity, organisation and efficency.  



=== Global and local project functions ===

Functions that can be used across any project should be put into a 'global-utils.py' file.  
Local functions that are project specific should be included inside a project-local 'local-utils.py' file. 



=== A generalised Data Analytics workflow ===

1. Jupyter notebook: Develop, debug and experiment in Jupyter. Take non-general, project specific functions here and move to 'local-utils.py'. If you edit 'local-utils.py' while the notebook is running use %load_ext autoreload to re-load the edited package.    
3. Pycharm: Make generalised tasks you are doing many times in Jupyter into functions 'global-utils.py' to use in the future. Clean data in Pycharm if it's easier. Write automation scripts here.   
4. Tableau/PowerBI: Use in the final stages for visualisation and dashboards. 

For example, a the data-analytics-portfolio may contain a project folder with the following:

    📁 project/
    ├── data/
    │   └── raw_data.csv
    ├── notebooks/
    │   └── 01_eda.ipynb
    │   └── 02_modeling.ipynb
    ├── scripts/
    │   └── clean_data.py
    │   └── local-utils.py
    ├── visuals/
    │   └── dashboard.pbix   ← (Power BI file)
    │   └── tableau_dashboard.twbx
    └── README.md
