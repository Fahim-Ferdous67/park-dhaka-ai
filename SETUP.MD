# Setup & Installation Instructions

Follow these steps to deploy your own instance of ParkDhaka:

### 1. Database Setup
1. Create a **Google Sheet** with columns: `ID`, `Lot_Name`, `Total_Slots`, `Available_Slots`, `Price`, and `AI_Prediction`.
2. Go to `File > Share > Publish to Web`.
3. Select the sheet and set the format to **CSV**. Copy this link.

### 2. Automation Logic (Make.com)
1. Create a new Scenario in **Make.com**.
2. Add a **Custom Webhook** as the trigger.
3. Connect it to a **Google Sheets (Update a Row)** module to manage the slot counts.
4. (Optional) Add a **Gemini AI** module to generate predictions based on the row data.

### 3. Frontend Deployment
1. Fork this repository.
2. In `index.html` and `owner.html`, replace the `SHEET_CSV_URL` and `WEBHOOK_URL` variables with your specific links.
3. Go to `Settings > Pages` in your GitHub repo and enable **GitHub Pages** on the main branch.
4. Your apps will be live at `https://<your-username>.github.io/park-dhaka-ai/`.

### 4. Stage Demo Mode
* Open the Owner App on a desktop.
* Press the **'N'** key to simulate a live customer booking notification for demo purposes.
