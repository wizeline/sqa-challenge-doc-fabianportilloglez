# **Overview:**

[**MkDocs**](https://www.mkdocs.org/) is a fast, simple and static site generator for building project documentation. 

Documentation source files are written in [**Markdown**](https://www.markdownguide.org/getting-started/), and configured with a single YAML configuration file to add the structure and navigation menus. 

**Example:**

mkdocs.yml file:
```
# Paths and navigation.
nav:
    - Home: index.md
    - Introduction:
      - 'Introduction': 'Introduction/intro-doc.md'
    - Documentation:
      - 'Docs': 'Documentation/doc-steps.md'  
      ...
```

___
# **Installation**

!!! important
    If you face any issue along this installation process then you can go here: [**Troubleshooting**](https://squidfunk.github.io/mkdocs-material/troubleshooting/) to solve it easily.

### **1.- Verify 'python' and 'pip' locally**

#### **1.1 Verify python:**
You can check if you have these already installed from the command line:

```python --version```

...*Python 2.7.16*

#### **1.2 Verify pip/pip3:**
Now, if you're familiar with Python, you can install Material and MkDocs with pip , the Python package manager.
Make sure you have it installed in your computer using:

```pip --version``` or ```pip3 --version```.

### **2.- Install Mkdocs**

Install the Mkdocs package using pip:

```pip3 install mkdocs```

Once is done, to check that everything worked fine run:

```mkdocs --version```

you will see something like: 
*mkdocs, version 1.1 from /Library/Python/3.7/site-packages/mkdocs (Python 3.7)*
___
### **3.- Install 'Material' theme for Mkdocs**

```pip3 install mkdocs-material```

### **4.- Install git plugin**

```pip3 install mkdocs-git-revision-date-plugin```

This plugin will allow you to see the date of documentation updates.

### **5.- Clone the Github repo**

```git clone git@github.ibm.com:wizeline/YOUR_REPO.git```

### **6.- Test the site locally**

MkDocs comes included with a server. 
In order to run the site locally, inside your project use:

```mkdocs serve```

Then Open up [**http://127.0.0.1:8000/**](http://127.0.0.1:8000/) in your browser, and you will see the default Home Page to verify all the time how looks everything before push your changes.

### **Done!**