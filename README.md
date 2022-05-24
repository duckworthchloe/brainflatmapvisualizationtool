# brainflatmapvisualizationtool
1. On Github, click the green “Code button” and select “Download Zip”
2. Open the .zip file downloaded, which will unzip the file and create a folder called “brainflatmapvisualizationtool-main”
3. Sign into a Google account and open Drive. In Drive, open the “My Drive” folder on the left side menu.
4. In the top left corner, select the “+ New” button, then “Folder Upload” and select the “brainflatmapvisualizationtool-main” folder that you just downloaded, then select “Upload” once more.
5. Once uploaded, open the “brainflatmapvisualizationtool-main” folder and open the folder for the animal model you’d like to work with. Then open its InputtedData.xlsx file.

a) Note: these instructions with be using the rat model as an example, but the steps are the same for the mouse and human maps as well.
6. To input your specific data, enter your values in the “Data Value” columns for the left and right side under “Data Entry (user entered)”. All brain regions left blank will remain grey, all zero values will be printed blue, and the rest of the numerical values will be slotted into one of 7 buckets: very weak, weak, weak-moderate, moderate, moderate-strong, strong, very strong.

a) Note: you can input data in any order of regions as long as you only edit the values under “Data Entry (user entered).” You don’t have to give data for the same regions on each side.

b) The map’s default is to use equally spaced bins with the minimum starting at your lowest value and the maximum being your highest value. If you would like to define your own bin values for the heatmap, change only the values under “(<=) high” and ensure all the data values you input are included in your chosen range, or else the outliers will be excluded from the map. 
7. Once you’ve inputted all the data you’d like to, open the file “ratFlatmap.ipynb”

a) If this automatically opens the file, proceed to step 8.

b) If you see a screen with the button “Open with Colaboratory” at the top, select that button.

c) If you see a screen with a “Download” button and another “Open with” button at the top, select “Open with” and then “Connect more apps.” In the window that appears, select the search button, and search for “Colaboratory”. Select the “Colaboratory” icon that appears and the “Install” button after that. When prompted for permission, select “Continue” and sign into the Google account that you are using. Once installed, refresh the window, and the code should open in Colaboratory.  
8. We will now be playing a few cells in Colaboratory to run the code. To “play” a cell, hover over the set of brackets in the top-left corner of the cell (labeled 1-3 above each cell). Once you’ve hovered over the brackets, a play button will appear, which you will click to run the cell. You will know that the cell is done running when then the loading circle around the brackets stops.
9. Play cells 1 and 2. You will see that a message output appears while the cell is still playing. In order for the cell to finish running, you must click the link that is displayed in the message output. This is to give Google permission to change the flatmap’s colors using this code. Ensure that you are signed into the same Google account that you used to run the code. Copy the authorization code displayed by Google, and paste it into the empty box in the cell’s output message, under “Enter the authorization code:” You will need to CTRL-V on a PC or Command-V on a Mac device. Once pasted, hit “Enter” or “Return” on your keyboard.
10. Play cell 3, and wait approximately 75 seconds for the cell to finish running. You will know that it’s done when the loading bar on the play button disappears and when the bottom bar’s message switches from “Executing” to “Completed”
11. View your updated heatmap in the “brainflatmapvisualizationtool-main” folder as “ratFlatmap.svg” (if you wish to further edit the file outside of Google Drive”) or “ratFlatmap.pdf” (for a finalized exportable version). You will also see the version with labels, “ratFlatmapWithKey.pdf”. The Google preview rendering will appear blurry, but the full resolution file is available once you download it to your computer. 
