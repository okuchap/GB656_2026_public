# GB656 2026 student materials

This public repository contains the datasets, lab notebooks, and problem-set
templates released to students in GB656.

Students do not need to clone this repository or use Git. GitHub hosts the released
files, Google Colab runs the notebooks, and Google Drive stores each student's
editable problem-set copy.

## Released materials

| Module | Item | Topic | Status | Open in Colab |
|---|---|---|---|---|
| 2 | Problem Set 1 template | Simple linear regression | Released | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/okuchap/GB656_2026_public/blob/main/problem-sets/02-01-template.ipynb) |
| 2 | Problem Set 1 lab | Simple linear regression workflow | Released | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/okuchap/GB656_2026_public/blob/main/problem-sets/lab-lectures/02-01-lab.ipynb) |
| 3 | Problem Set 2 template | Multivariate linear regression | Released | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/okuchap/GB656_2026_public/blob/main/problem-sets/03-02-template.ipynb) |
| 3 | Problem Set 2 lab | Multivariate linear regression workflow | Released | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/okuchap/GB656_2026_public/blob/main/problem-sets/lab-lectures/03-02-lab.ipynb) |

Labs are practice and are not submitted unless the instructor says otherwise.
Saving a Drive copy of a lab is optional.

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

The notebooks first look for course data in a local clone and otherwise load the
same files automatically from this public repository. Students working in Colab do
not need to upload data or mount Google Drive. Dataset sources, transformations,
checksums, and upstream licensing declarations are documented in
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
