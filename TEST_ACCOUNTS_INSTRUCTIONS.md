# Test Accounts Setup Instructions

## Why Only ethiocapitalx@gmail.com and test010@gmail.com Work

Currently only these 2 accounts work because they have REAL Firebase authentication:
- `ethiocapitalx@gmail.com` - Real Firebase UID: `4b9YqLck4eRtproC5sQbVknx9lj1`
- `test010@gmail.com` - Real Firebase UID: `h0y156GG1JZFCsXPEUnX3NtW6jH3`

The other test accounts (Test001-Test009) have fake Firebase UIDs that only work for API testing, not real frontend login.

## Solution: Create Real Firebase Accounts

To make ALL test accounts work in the frontend, you need to:

### Option 1: Use Existing Gmail Accounts
1. Sign up for Firebase accounts using these emails:
   - test001@gmail.com
   - test002@gmail.com
   - test003@gmail.com
   - test004@gmail.com
   - test005@gmail.com
   - test006@gmail.com
   - test007@gmail.com
   - test008@gmail.com
   - test009@gmail.com

2. When they sign in the first time, the system will automatically give them their custom balances:
   - test001@gmail.com → $1200.00 balance
   - test002@gmail.com → $980.00 balance
   - test003@gmail.com → $720.00 balance
   - test004@gmail.com → $1800.00 balance
   - test005@gmail.com → $650.00 balance
   - test006@gmail.com → $2100.00 balance
   - test007@gmail.com → $1100.00 balance
   - test008@gmail.com → $900.00 balance
   - test009@gmail.com → $420.00 balance

### Option 2: Alternative Email Addresses
If you can't create Gmail accounts with those exact emails, you can:
1. Create any Firebase accounts with different emails
2. Update the special user configuration in `server/routes.ts` to include your new email addresses
3. The system will automatically apply custom balances when they sign in

## Current Working Status
✅ ethiocapitalx@gmail.com - $1742.00 balance (WORKING)
✅ test010@gmail.com - $3000.00 balance (WORKING)
⚠️ test001@gmail.com through test009@gmail.com - Need real Firebase accounts

## Technical Details
- Backend API works perfectly for all accounts
- Custom balance system is fully functional
- Only missing: Real Firebase authentication for Test001-Test009
- System automatically detects special emails and applies custom balances on first login