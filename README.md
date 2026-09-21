# GB656 2026 student materials

This public repository contains the datasets and Jupyter notebooks released in
GB656, including problem-set templates, labs, and Module 7 application exercises.

Students do not need to clone this repository or use Git. GitHub hosts the released
files, Google Colab runs the notebooks, and Google Drive stores each student's
editable problem-set copy.

## Released materials

| Module | Item | Topic | Open in Colab |
|---|---|---|---|
| 2 | Problem Set 1 template | Simple linear regression | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/okuchap/GB656_2026_public/blob/main/problem-sets/02-01-template.ipynb) |
| 2 | Problem Set 1 lab | Simple linear regression workflow | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/okuchap/GB656_2026_public/blob/main/problem-sets/lab-lectures/02-01-lab.ipynb) |
| 3 | Problem Set 2 template | Multivariate linear regression | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/okuchap/GB656_2026_public/blob/main/problem-sets/03-02-template.ipynb) |
| 3 | Problem Set 2 lab | Multivariate linear regression workflow | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/okuchap/GB656_2026_public/blob/main/problem-sets/lab-lectures/03-02-lab.ipynb) |
| 4 | Problem Set 3 template | Credit-card default review policy | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/okuchap/GB656_2026_public/blob/main/problem-sets/04-03-template.ipynb) |
| 4 | Problem Set 3 lab | Logistic regression workflow | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/okuchap/GB656_2026_public/blob/main/problem-sets/lab-lectures/04-03-lab.ipynb) |
| 5 | Problem Set 4 template | Cross-validation and model selection | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/okuchap/GB656_2026_public/blob/main/problem-sets/05-04-template.ipynb) |
| 5 | Problem Set 4 lab | Cross-validation and forward selection | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/okuchap/GB656_2026_public/blob/main/problem-sets/lab-lectures/05-04-lab.ipynb) |
| 6 | Problem Set 5 template | Residential sales-price regularization | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/okuchap/GB656_2026_public/blob/main/problem-sets/06-05-template.ipynb) |
| 6 | Problem Set 5 lab | Regularization and hyperparameter-tuning workflow | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/okuchap/GB656_2026_public/blob/main/problem-sets/lab-lectures/06-05-lab.ipynb) |
| 7 | Application Section 2 | Understand the synthetic patient-year data | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/okuchap/GB656_2026_public/blob/main/module_7/07-02-understand-data.ipynb) |
| 7 | Application Section 3 | Audit recorded active chronic conditions | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/okuchap/GB656_2026_public/blob/main/module_7/07-03-audit-illness.ipynb) |
| 7 | Application Section 4 | Investigate what the risk score tracks | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/okuchap/GB656_2026_public/blob/main/module_7/07-04-audit-cost.ipynb) |
| 7 | Application Section 5 | Rebuild and compare the ranking | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/okuchap/GB656_2026_public/blob/main/module_7/07-05-rebuild-models.ipynb) |

Labs are practice and are not submitted unless the instructor says otherwise.
Saving a Drive copy of a lab is optional.

The Module 7 application notebooks are sequential in-class exercises.

## Complete and submit a problem set

1. Open the appropriate problem-set template using its Colab link above.
2. Before editing, select **File > Save a copy in Drive**.
3. Work only in the saved copy and rename it so the filename includes the problem-set
   number and your name.
4. Complete every code and written-response task.
5. Select **Runtime > Run all**. Confirm that every requested output is visible and
   no cell reports an error, then save the notebook.
6. Click **Share**. Under **General access**, choose **Anyone with the link**, set the
   role to **Viewer**, and copy the sharing link.
7. Submit the link to the completed Drive copy as the **Website URL** in Canvas. Do
   not submit the original GitHub template link.
8. After the deadline, do not edit the submitted notebook unless the instructor asks
   you to resubmit.

## Data

Most notebooks first look for course data in a local clone and otherwise load the
required file automatically from a public source. Problem Sets 1–5 and their labs
use files in this repository, except that the Problem Set 3 lab loads its
customer-churn data from a pinned IBM source. The Module 7 notebooks load a public
synthetic patient-year dataset from a pinned Dissecting Bias source on GitLab.
Students working in Colab do not need to upload data or mount Google Drive. Dataset
sources, transformations, checksums, and upstream terms are documented in
[`data/README.md`](data/README.md).

## Troubleshooting

- If your changes disappear, confirm that you selected **File > Save a copy in
  Drive** and are editing that copy.
- If a data-loading cell fails, reopen the notebook from the Colab link above, check
  that the runtime has internet access, and rerun the instructor-provided setup and
  loading cells without changing the repository name or filename.
- Before submitting, open the sharing link in a private/incognito browser window. It
  should display the completed notebook without requesting access.
- For a broken course link or an assignment-specific question, contact the
  instructor through Canvas.
