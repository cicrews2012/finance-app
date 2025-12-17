# finance-app

URL: https://cicrews2012.github.io/finance-app/



**Current Version:** v1.1.0

## How to Use

### First Time Setup

1. **Add Recurring Payments** (Optional but recommended)
   - Expand "Recurring Payments" section
   - Click "Add Recurring Payment"
   - Enter name, amount, category, due day
   - Choose if it auto-adds or requires manual marking
   - Mark if amount varies monthly

2. **Add Debts** (If applicable)
   - Expand "Debt Tracker" section
   - Click "Add Debt"
   - Enter debt name, current balance, APR, monthly payment, due day
   - The system will track payoff projections automatically

3. **Start Adding Transactions**
   - Expand "Add Transaction" section
   - Choose income or expense
   - Enter description, amount, category, and date
   - Click "Add Transaction"

### Daily Use

**Adding a Transaction:**
1. Click "Add Transaction" section to expand
2. Fill in the form (type, date, description, amount, category)
3. Click "Add Transaction"
4. If it matches a debt payment, balance updates automatically

**Marking Recurring Payments:**
1. Expand "Recurring Payments" section
2. Find the payment due
3. Click "Mark as Paid"
4. Transaction is created automatically
5. Debt balances update if applicable

**Editing a Transaction:**
1. Scroll to monthly transactions
2. Expand the month with the transaction
3. Click the blue pencil icon next to the transaction
4. Form opens with transaction details
5. Make changes and click "Update Transaction"

**Viewing Spending by Category:**
1. Expand "Yearly Category Analysis"
2. Click any category to see individual transactions
3. Review what you spent in that category

### Data Management

**Export Your Data:**
1. Click "Export Data" button (top right)
2. JSON file downloads with today's date
3. Save this file somewhere safe (cloud storage, USB drive, etc.)

**Import Your Data:**
1. Click "Import Data" button
2. Select your previously exported JSON file
3. All your transactions, debts, and recurring payments load
4. Continue where you left off

**Best Practice:**
- Export weekly or monthly
- Keep multiple backups
- Before clearing data, always export first

**Clear All Data:**
1. Click "Clear All Data" button
2. Type "yes" to confirm
3. Everything is deleted from browser storage
4. Fresh start (import your backup to restore)

## Tips & Tricks

### Recurring Payment Automation
- When you mark a recurring payment as paid, it creates the transaction automatically
- If the payment also matches a debt name, it reduces the debt balance
- Name your recurring payments exactly like your debts for auto-linking (e.g., "Mortgage", "Car Loan")

### Smart Debt Linking
The system automatically links payments to debts when:
- Payment name matches debt name (even partially, e.g., "SZC" matches "SZC Car")
- Payment category is debt-related: "Debt", "Car Payments", "Home", or "Personal"
- Both conditions must be true to prevent false matches

### Custom Categories
- Select "+ Custom Category" when adding a transaction
- Type the category name
- It's automatically saved for future use
- Manage custom categories in the "Custom Categories" section at bottom

### Financial Month Understanding
- Runs from 28th of one month to 27th of next month
- Example: November financial month is Oct 28 - Nov 27
- Helps align budget cycles with paychecks

### Collapsible Interface
- All sections start collapsed to reduce clutter
- Click any section header to expand/collapse
- Monthly transactions also collapse - click month headers to expand

## Troubleshooting

**Data Not Showing After Import:**
- Refresh the page after importing
- Check the JSON file is the correct v2.0 format
- Make sure file isn't corrupted

**Transactions Not Showing in Summary:**
- Check the financial month dates (28th-27th cycle)
- Verify transactions have both financialMonth and financialYear fields
- Re-import your data if fields are missing

**Debt Not Auto-Linking:**
- Check payment name matches debt name
- Verify payment category is "Debt", "Car Payments", "Home", or "Personal"
- Check spelling matches (system normalizes names but they should be similar)

**Browser Storage Full:**
- Export your data
- Clear all data
- Import only what you need (recent months)
- Or split data by year

## Browser Compatibility

- ✅ Chrome/Edge (recommended)
- ✅ Firefox
- ✅ Safari
- ✅ Mobile browsers (iOS Safari, Chrome Mobile)

Requires modern browser with JavaScript enabled.

## Privacy & Security

- **100% Local**: All data stored in your browser's localStorage
- **No Server**: No data sent to any server
- **No Tracking**: No analytics or tracking scripts
- **No Account**: No registration or login required
- **Your Control**: You own your data completely

**Important Notes:**
- Data is tied to the browser and domain
- Clearing browser data will delete your information
- Use Export regularly to back up
- Private/Incognito mode won't save data between sessions

## Technical Details

**Built With:**
- React 18 (via CDN)
- Tailwind CSS (via CDN)
- Vanilla JavaScript
- Browser localStorage API

**File Format:**
- Single HTML file
- No build process required
- No npm/node_modules needed
- Works offline after initial load

**Data Format (v2.0):**
```json
{
  "version": "2.0",
  "exportDate": "2025-12-17T...",
  "transactions": [...],
  "debts": [...],
  "recurringPayments": [...],
  "paidRecurring": {...},
  "customExpenseCategories": [...],
  "customIncomeCategories": [...]
}
```

## Version History

### v1.1.0 (Current)
- Added edit transaction functionality
- All sections default to collapsed
- Clickable categories in yearly analysis with transaction drill-down
- Collapsible monthly transaction sections
- Added recurring payment indicator (🔄) in monthly view
- Version number display in UI

### v1.0.0
- Initial standalone release
- Transaction tracking with monthly breakdown
- Debt tracker with payoff projections
- Recurring payment management
- Yearly category analysis
- Export/import functionality
- Custom categories
- Zero hardcoded data

## Support

For issues, questions, or feature requests:
1. Check this README first
2. Try exporting and reimporting your data
3. Clear browser cache if issues persist
4. Start fresh and import backup if needed

## License

This is personal finance tracking software provided as-is for personal use.

---

**Current Version:** v1.1.0  
**Last Updated:** December 2025
