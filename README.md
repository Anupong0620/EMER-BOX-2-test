# EMER-BOX-2-test
Emergency Med Box Tracker (HTML + Apps Script)

Quick Start
-----------
1) Google Sheet: create two tabs EXACTLY:
   - Inventory: headers in row 1 = Box | Drug | EXP | Qty
   - Transactions: leave empty; headers will be written automatically

   Tip: Use date format YYYY-MM-DD for EXP.

2) Apps Script (Extensions → Apps Script):
   - Create a new script and paste Code.gs (this repo).
   - Deploy → New deployment → Web app
     * Execute as: Me
     * Who has access: Anyone with the link
   - Copy the Web app URL.

3) Frontend:
   - Open index.html and replace API_BASE = 'YOUR_WEB_APP_URL' with your URL.
   - Open index.html locally to test OR push to GitHub Pages.

4) Usage:
   - Page 1: select a box (e.g., IPD01/ER01/... or type your own).
   - Page 2: choose a drug, click "โหลดล็อตจากสต็อก" to see existing lots, set "ใช้ไป" or "ลบล็อตนี้", add new lots with different EXP, then Save.
   - Page 3: shows near-expiry items for the selected box.

Notes
-----
- If you face CORS issues, either:
  a) Host index.html via Apps Script HtmlService in the same project, OR
  b) Use a tiny proxy (e.g., Cloudflare Workers) between your static site and Apps Script.
- Data logs are recorded in the Transactions sheet for audit.

## 📘 คู่มือการใช้งานระบบ EMER-BOX

- [เปิดคู่มือส่วนลงข้อมูล (PDF)](https://github.com/Anupong0620/EMER-BOX-2-test/blob/main/EMER-BOX-MANUAL1.pdf)
- [เปิดคู่มือส่วนหน้าแสดงผล (PDF)](https://github.com/Anupong0620/EMER-BOX-2-test/blob/main/EMER-BOX-MANUAL2.pdf)
