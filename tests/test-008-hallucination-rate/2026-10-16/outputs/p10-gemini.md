Microsoft Excel does not have a built-in feature called **Formula Diary** on the Review tab (or anywhere else in the program).

However, if you are looking to keep a chronological log or "diary" of edits made to formulas and values, or if you want to monitor formulas as they update, you are likely looking for one of three actual Excel features: **Show Changes** (located on the Review tab), **Track Changes (Legacy)**, or the **Watch Window** (located on the Formulas tab).

---

### 1. How to Use "Show Changes" (Review Tab)

In Microsoft 365, **Show Changes** acts like an automatic diary for your workbook, logging exactly who changed a formula or value, when they did it, and what the previous formula was.

1. **Save the file to the cloud:** Prerequisite - Show Changes only works on OneDrive or SharePoint.
Make sure your workbook is saved to **OneDrive** or **SharePoint** and that **AutoSave** is turned on in the top-left corner.


2. **Open the Review tab:**
Click **Review** in the top ribbon.


3. **Click Show Changes:**
In the **Changes** group, select **Show Changes**. A pane will open on the right side of your screen displaying a chronological log of all recent formula and value edits.


4. **Filter for a specific cell or range:** Optional.
To see the history of a single formula, right-click that specific cell and select **Show Changes** from the context menu.


---

### 2. How to Enable "Track Changes (Legacy)" for a History Sheet

If you are working on a local file (not on OneDrive) and want Excel to generate a dedicated **History worksheet** that acts like a diary of all formula edits, you have to re-enable the hidden legacy feature on the Review tab:

1. Click **File** and select **Options**.
2. Select **Customize Ribbon** on the left menu.
3. On the right side under **Main Tabs**, expand **Review**, right-click it, and select **Add New Group**.
4. On the left side, change the **Choose commands from** dropdown to **Commands Not in the Ribbon** (or **All Commands**).
5. Scroll down, select **Track Changes (Legacy)**, click **Add** to move it into your new Review group, and click **OK**.
6. Go to the **Review** tab, click **Track Changes (Legacy)**, and select **Highlight Changes**.
7. Check **Track changes while editing** (this will save the workbook as a Shared Workbook) and click **OK**.
8. Once edits have been made, return to **Highlight Changes**, check **List changes on a new sheet**, and click **OK** to generate a dedicated **History** tab.

---

### 3. How to Use the "Watch Window" (Formulas Tab)

If your goal is to keep a live "diary" panel open to monitor specific formulas across different sheets as you update your workbook:

1. Go to the **Formulas** tab on the ribbon.
2. In the **Formula Auditing** group, click **Watch Window**.
3. Click **Add Watch...** in the panel that appears.
4. Select the cells containing the formulas you want to keep an eye on and click **Add**. The panel will continuously display the workbook, sheet, cell, current value, and exact formula in real time.
