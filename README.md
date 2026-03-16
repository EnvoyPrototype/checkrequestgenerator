# Check Request Form
### Carpenter's Homelessness Prevention Program

A browser-based check request form that can be filled out digitally, printed, or exported as a PDF for DocuSign routing — no backend or installation required.

🔗 **[Live Form → envoyprototype.github.io/checkrequestgenerator](https://envoyprototype.github.io/checkrequestgenerator/)**

---

## Features

- **Auto-generated date** — Today's date fills automatically; "Needed By" defaults to today but can be changed to any future date
- **Dropdown menus** — Pre-populated options for Special Project/Grant and Budget Expense Line
- **Payment method selection** — Required radio button choice between Mail/Direct Deposit and Hold for Pickup
- **Auto-calculating total** — Amount field updates the TOTAL automatically as you type
- **DocuSign-ready** — The Approved By field includes a hidden `/sn1/` anchor tag so DocuSign auto-places a signature field when the PDF is uploaded
- **Required field validation** — Highlights missing required fields before allowing print
- **One-page print layout** — Formatted to fit on a single letter-size page
- **Office use section** — "To Pay from Bank Account" and "PAID" boxes are inert on screen but print cleanly for manual office use
- **Clear form button** — Resets all fields back to defaults

---

## Usage

### Filling Out the Form
1. Open `check_request_form.html` in any modern web browser
2. Complete all required fields (marked with a red `*`):
   - Payable To
   - Special Project / Grant to Charge
   - Budget Expense Line to Charge
   - Description & Amount
   - Payment Method
   - Last, First Name (check memo)
   - Prepared By
3. Click **Print / Save as PDF**

### Printing a Physical Copy
- Click **Print / Save as PDF**
- In the print dialog, select your printer
- The Approved By line will print as a blank signature line
- The form is pre-formatted to fit one letter-size page

### Saving as a PDF
- Click **Print / Save as PDF**
- In the print dialog, choose **Save as PDF** (or **Microsoft Print to PDF** on Windows)
- Save the file

### Sending via DocuSign
1. Fill out the form and save as a PDF (see above)
2. Log in to [DocuSign](https://www.docusign.com)
3. Click **Send an Envelope** and upload the PDF
4. DocuSign will detect the `/sn1/` anchor tag and automatically place the signature field on the **Approved By** line
5. Add your recipient and send

---

## Form Fields

| Field | Required | Notes |
|---|---|---|
| Payable To | ✅ | 3–4 line text area for payee name/address |
| Today's Date | — | Auto-fills, read-only |
| Needed By | — | Defaults to today; future dates selectable |
| Payment Method | ✅ | Radio: Mail/Direct Deposit or Hold for Pickup |
| Special Project / Grant | ✅ | Dropdown |
| Budget Expense Line | ✅ | Dropdown |
| Acct # | — | Optional account number |
| Description | ✅ | Line item description |
| Amount | ✅ | Auto-adds to TOTAL |
| Last, First Name | ✅ | For check memo |
| Prepared By | ✅ | Name of form preparer |
| Approved By | — | DocuSign / physical signature field |

---

## Dropdown Options

**Special Project / Grant to Charge**
- ILRRH TBRA
- ILRRH HRSS
- ESG RRH TBRA
- ESG RRH HRSS

**Budget Expense Line to Charge**
- 6740-1 Rental Assistance
- 6740-2 Security Dep/Application
- 6740-3 Utilities Assistance
- 6740-4 Mortgage Assistance
- 6740-5 Hotels

---

## Customization

All options are defined directly in the HTML file and can be edited without any build tools.

**To add/edit dropdown options** — Search for `<select id="project-grant">` or `<select id="budget-line">` and add/remove `<option>` lines.

**To add more description rows** — Duplicate the `<tr>` block inside `<tbody id="desc-rows">`. New amount fields will automatically be included in the total calculation.

**To add/edit payment method options** — Search for `name="payment-method"` and add/remove `<label class="radio-label">` blocks.

**To update the organization name** — Search for `Carpenter's Homelessness Prevention` and replace as needed.

---

## Browser Compatibility

Works in all modern browsers. No internet connection required after the file is downloaded (except for loading the Google Fonts stylesheet, which degrades gracefully).

| Browser | Supported |
|---|---|
| Chrome / Edge | ✅ |
| Firefox | ✅ |
| Safari | ✅ |

---

## File Structure

```
check_request_form.html   # Single self-contained file — HTML, CSS, and JS
README.md                 # This file
```

---

## License

Internal use — Carpenter's Homelessness Prevention Program.
