# Brain Flatmap Visualization Tools Instructions

**Instructions updated September 2026**

Please note: These instructions are periodically revised and updated from the originally published version to account for dependency or other changes associated with the code that are intended to ensure its continuing operation. Please refer to the current instructions given below. Notebook copies downloaded previously are not updated automatically.

## File setup (steps 1–5, for tools first use)

1. The brain flatmap visualization tools require a Google Account and a modern web browser (Google Chrome recommended). If you do not already have a Google Account, visit the following link to create one: [https://accounts.google.com/signup/v2/webcreateaccount?flowName=GlifWebSignIn&flowEntry=SignUp](https://accounts.google.com/signup/v2/webcreateaccount?flowName=GlifWebSignIn&flowEntry=SignUp).

2. Files required to run the flatmap tools are stored as a repository on GitHub (a popular website for open-source software development). A GitHub account is not required to access the files, which are available at: [https://github.com/duckworthchloe/brainflatmapvisualizationtool](https://github.com/duckworthchloe/brainflatmapvisualizationtool). Select the green **Code** button and then select **Download ZIP**.

   If you have not used the flatmap tools recently, first back up any input spreadsheets containing data that you wish to retain. Rename, move, or archive any older version of the `brainflatmapvisualizationtool-main` folder in Google Drive, and then download the current version from GitHub. Do not delete an input spreadsheet until you have preserved any data that you wish to retain.

3. Locate and open the ZIP file you downloaded (file name: `brainflatmapvisualizationtool-main`). This will open the ZIP file contents to show an unzipped folder with the same name as the ZIP file. Drag and drop or copy and paste the unzipped folder to an accessible folder on your computer. Do not rename the unzipped `brainflatmapvisualizationtool-main` folder or place it inside another folder with the same name.

4. Open your web browser and sign into your Google Account, then in Google Drive open the **My Drive** folder (left side menu) or follow this link: [https://drive.google.com/drive/my-drive](https://drive.google.com/drive/my-drive).

5. In the top left corner, select the **+ New** button, then select **Folder upload**, then locate and select the unzipped `brainflatmapvisualizationtool-main` folder on your computer and select **Upload** to upload the folder directly to **My Drive**.

- Steps 1–5 typically only need to be performed once for the same Google Account, except when replacing an older version of the tools.

## Data entry (steps 6–8)

6. After the folder `brainflatmapvisualizationtool-main` has finished uploading to your Google Drive, open the folder and then open one of the `Rat`, `Mouse`, or `Human` subfolders according to your preference/data. A document file named README with these instructions is included in the repository.

- The following steps use the Rat flatmap as an example; the same steps apply to Mouse and Human.

7. In the `Rat` folder, open the file `ratinputtedData.xlsx` (equivalent files for Mouse and Human are named accordingly) using Google Sheets. Edit the existing `.xlsx` spreadsheet and retain its original filename and Excel format. Do not select **Save as Google Sheets** or create a separate native Google Sheets version, because the Colaboratory notebook reads the `.xlsx` file stored in the species folder. This step only needs to be performed once for each data-entry session.

8. Data entry is performed on the first sheet of the `ratinputtedData.xlsx` spreadsheet. Enter your data according to region abbreviation and data values. These may be entered individually or copied and pasted from your own spreadsheet, or elsewhere. If copying and pasting, to avoid altering the sheet formatting, perform the paste operation as **Values only**, using the following Google Sheets menu/selection sequence: **Edit → Paste special → Values only** (the keyboard shortcut for this operation is **Ctrl+Shift+V**). Data-entry columns are provided for both sides of the brain, **Left side or side 1** and **Right side or side 2**. If your data apply to one side only, then enter them on that side only.

- In addition to allowing for entry of bilateral data, the data-entry columns for the two sides may also be used to represent different sets of data for comparative purposes (for example, including two sets of data from the same brain side).

- Data entered for side 1 (or left side) will appear on the bottom half of the flatmap diagram; side 2 (or right side) data will appear on the top half. Region names and abbreviations are listed for reference on the second sheet, `Region names`, in alphabetical and topographic arrangements. Abbreviations must be entered exactly as shown on the `Region names` sheet to enable correct data processing. As the data are entered, the processed data will appear in gray-shaded columns to the right of the `Data Entry` column, and basic summary statistics for the data will appear above them.

- An exception to numerical data entry is enabled to indicate an experimental site (for example, the site of an injection or other manipulation). For this purpose, enter the text `SITE` in the Data Value column for the experimental site region or regions. These entries will be rendered in a different color from the other data on the flatmap. By default, data entered are assigned to seven equally spaced bins, calculated according to the maximum and minimum data values. To define a different bin range, use the top-left table on the `Data entry` sheet. As indicated on the bin-range table annotation, user-defined bins 2–7 are entered in the column titled `(<=) high` in an ascending sequence sufficient to include the highest value in your dataset.

- If your data include both positive and negative values, the sign of the negative values must first be reversed (numbers converted to positive integers), and these should then be entered either on a separate sheet or using the two-side option described above. Additionally, for comparative purposes, different side data can be binned separately, either automatically when the default equally spaced bin range is used, or user-defined.

- If data are entered for both sides of the brain (or both data columns are used), by default the same bin range (user-defined or default equally spaced) will apply to all the data. However, for comparative purposes (for example, data from different experiments), the data for each side can be automatically binned separately when the default bin range is used. To enable this option, select `yes` from the dropdown menu in the column to the right of the bin-range table at top left.

- To apply a different user-defined bin range to each side data column, first enter data for one side using the first user-defined bin range, then copy and paste the `Region Abbreviation` and `Data Value (binned)` columns from the auto-processed data columns (gray shaded) to a different spreadsheet. Next, clear the entered data and repeat these steps with the second set of data and second user-defined bin range. Then again clear the data-entry columns, clear the user-defined bin range, and paste the two copied sets of data each to a different side of the Data Entry columns. Before proceeding to generate the flatmap, ensure that the option to bin side data separately is set to `no`.

## Flatmap generation (steps 9–11)

9. When you have finished entering data, remain in the appropriate `Rat`, `Mouse`, or `Human` subfolder in `brainflatmapvisualizationtool-main` in your Google Drive and open the corresponding notebook file (for example, `ratFlatmap.ipynb` for Rat). Opening the `.ipynb` file will open the code document in a new browser tab in Google Colaboratory. If you are prompted with an **Open with Colab** button at the top of the page, select it. If this opens the notebook, proceed to step 10; otherwise select **Connect more apps**, and in the window that appears select the **Search** button and search for `Colaboratory`. Then select the **Colaboratory** and **Install** buttons. When prompted for permission, select **Continue** and select/sign into the Google Account that you are using. After installation, refresh the browser window, and the code will open in Colaboratory.

10. You will now execute code in Colaboratory to generate the brain flatmap data diagram. To execute the code it is necessary to play code cells 1–3 in sequence. To perform this operation, from the **Runtime** menu at the top of the screen select **Run all**, or use the keyboard shortcut **Ctrl+F9**.

    When the code is executing, a play icon to the left of each code cell will be animated. Completion of code execution is indicated by a green check mark to the left of the play icon. Depending on your web browser and Google Account security settings, running the code may trigger one or more security dialogue boxes asking for your permission to execute the code and to access your Google Drive files. Mounting Google Drive allows code in the notebook to access files in the mounted Drive. This access is required so that the notebook can read the associated input files and save the generated outputs. Google controls these authorization prompts, and they may reappear when a new Colab runtime is started. Review the request and follow the prompts in the affirmative if you wish to proceed. Granting access may also generate automatic security notifications sent to your associated Google email account (Gmail).

    The notebook code is available for inspection in this GitHub repository. As provided, it reads the flatmap project input files and writes the generated output files; it does not send users' project data to the project authors.

- If you are generating more than one flatmap for the same species in the same session, it is necessary only to replay step 3 for each subsequent flatmap generated. To play only step 3, select/click the play icon for step 3.

11. After all three steps of the code have executed, the generated flatmap files will be deposited in the same `Rat`, `Mouse`, or `Human` subfolder containing the notebook.

- There is a latency associated with data input to the spreadsheet being sent to the Google cloud server and becoming accessible to the Colaboratory notebook (this is separate from the saving of files within Google Drive, which typically happens within a matter of seconds). For this reason, we recommend waiting five minutes after inputting your data before running the code. If the flatmap output does not show the expected result, wait an additional five minutes and then rerun the code.

Three files will be generated: `ratFlatmapWithKey.pdf`, `ratFlatmap.pdf`, and `ratFlatmap.svg`. These files can be previewed in the web browser and downloaded to your computer. The `ratFlatmapWithKey.pdf` file combines the flatmap with the overlay and color key. The other two files do not include the overlay. In addition to these files, separate overlay-only Adobe Illustrator and PDF files are also present in the `Rat` folder. All the files can be opened and edited for further customization in Adobe Illustrator or other PDF and SVG editing software, such as the open-source GNU Image Manipulation Program (GIMP) or Blender.

- If you are entering multiple datasets, to prevent use of cached data, after clearing the data it is recommended to close and reopen the data-entry spreadsheet and `.ipynb` file before entering new data.

## Troubleshooting

If Colaboratory reports that a file cannot be found, confirm that:

- The repository folder is named exactly `brainflatmapvisualizationtool-main`.
- It is located directly inside **My Drive**.
- The notebook remains inside the appropriate `Rat`, `Mouse`, or `Human` subfolder.
- The input spreadsheet, region SVG, and overlay PDF retain their original filenames.
- A second nested folder named `brainflatmapvisualizationtool-main` was not created during extraction or upload.

If the generated flatmap does not represent the data entered, confirm that you edited the existing `.xlsx` file rather than a separate native Google Sheets version. Close the spreadsheet, allow time for it to save, and rerun code cell 3. If the problem persists, download the data-containing spreadsheet as a Microsoft Excel (`.xlsx`) file and use it to replace the active species input spreadsheet, retaining the original required filename.

If the anatomical overlay does not align with the colored flatmap, confirm that you are using the latest notebook from this GitHub repository rather than a previously downloaded copy.

## Tested software environment

The September 2026 notebook update was tested in Google Colaboratory with:

- Python 3.13.15
- svglib 2.2.0
- reportlab 5.0.1
- PyPDF2 3.0.1

The notebooks install these tested package versions automatically. Additional packages supplied by the Google Colaboratory runtime are not forcibly reinstalled.

## Project contact

[brainflatmapviz@gmail.com](mailto:brainflatmapviz@gmail.com)
