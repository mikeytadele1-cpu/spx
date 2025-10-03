# Admin Panel Access Instructions

## How to Access the Admin Panel

### 1. Direct URL Access
- Navigate to: `YOUR_REPLIT_URL/admin`
- Example: `https://your-project.replit.dev/admin`

### 2. Navigation Menu
- The Admin link is available in the main navigation bar
- Click "Admin" in the top menu to access the admin dashboard

## Admin Panel Features

### Order Management
- **View Pending Orders**: See all orders waiting for verification
- **Verify Orders**: Approve orders after confirming payment
- **Reject Orders**: Reject orders with invalid payments
- **Activate Cards**: Activate cards and credit referral bonuses

### Withdrawal Management  
- **View Pending Withdrawals**: See all withdrawal requests
- **Approve Withdrawals**: Approve legitimate withdrawal requests
- **Reject Withdrawals**: Reject invalid withdrawal requests

## Admin Workflow

### For Orders:
1. User submits order with transaction hash (TXID)
2. Admin verifies payment on blockchain
3. Admin clicks "Verify" to approve order
4. Admin clicks "Activate Card" to activate and credit referral bonuses
5. User receives their card and referrer gets bonus

### For Withdrawals:
1. User requests withdrawal (minimum $100)
2. Admin reviews withdrawal request
3. Admin approves and processes payment
4. User balance is updated

## Current Admin Users
- All logged-in users can access admin panel (for demo purposes)
- In production, implement role-based access control

## Security Notes
- All admin actions are logged
- Transaction hashes should be verified on blockchain explorers
- Minimum withdrawal amount is $100
- Virtual card referrals pay $30, Physical card referrals pay $45