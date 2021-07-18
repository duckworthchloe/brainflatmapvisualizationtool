# brainflatmapvisualizationtool
1. On Github, click the green “Code button” and select “Download Zip”
2. Open the .zip file downloaded, which will unzip the file and create a folder called “brainflatmapvisualizationtool-main”
3. Sign into a Google account and open Drive. In Drive, open the “My Drive” folder on the left side menu.
4. In the top left corner, select the “+ New” button, then “Folder Upload” and select the “brainflatmapvisualizationtool-main” folder that you just downloaded, then select “Upload” once more.
5. Once uploaded, open the “brainflatmapvisualizationtool-main” folder and open the “ratInputtedData.xlsx” file.
6. To input your specific data, enter your values in the “Values” column. All brain regions left blank will remain grey, all values of zero will be printed black, and the rest of the numerical values will be slotted into one of 7 buckets: very weak, weak, weak-moderate, moderate, moderate-strong, strong, very strong.
    Note: do not change the values in “Abbreviation” column or the order of the rows because the order will be mixed up
7. Once you’ve inputted all the data you’d like to, open the file “ratFlatmap.ipynb”
8. The first time you ever open this file, you will need to click the play button on cell 1. After the first time, you will start running the code by playing cell 2.
9. Play cell 2, click the link that is displayed in the message output. This is to give Google permission to change the flatmap’s colors using this code. Ensure that you are signed into the same Google account that you used to run the code. Copy the passcode displayed by Google, and paste it into the empty box in the cell’s output message.
10. Play cell 3, and wait approximately 45 seconds for the cell to finish running. You will know that it’s done when the loading bar on the play button disappears and when the bottom bar’s message switches from “Executing” to “Completed”
11. View your updated heatmap in the “brainflatmapvisualizationtool-main” folder as “ex.svg”
