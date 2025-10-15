# Solana Validator Fee Tracker

A fast, modern web application that tracks Solana validator fee payments and outstanding debts across different epochs.

## Features

- **Data straight from the Source**: Fetches data directly from the [DoubleZero Foundation fees repository](https://github.com/doublezerofoundation/fees/blob/main/fees_and_payments.csv)
- **Dynamic Epoch Detection**: Automatically detects available epochs from CSV headers
- **Quick Overview**: Dashboard showing total validators, unpaid validators, epochs, and total debt
- **Detailed Tracking**: Table view showing fee status for each validator across all available epochs
- **Smart Filtering**: Filter by all validators, unpaid only, or paid only
- **Search Functionality**: Search by validator pubkey or Name
- **Responsive Design**: Works on desktop and mobile devices

## How to Use

1. **Open the Website**: Simply open `index.html` in your web browser
2. **View Summary Stats**: The top cards show key metrics at a glance
3. **Search Validators**: Use the search box to find specific validators
4. **Filter Results**: Click filter buttons to show all, unpaid, or paid validators
5. **Review Details**: The table shows fee status for each epoch with debt calculations

## Data Structure

The application processes CSV data with the following columns:
- `pubkey`: Validator's public key
- `votekey`: Validator's vote key
- `dz_fee_lamports_XXX`: Fee amount in lamports for each epoch
- `paid_XXX`: Payment status ("Yes" or "No") for each epoch

## Key Metrics

- **Total Validators**: Number of validators in the dataset
- **Unpaid Validators**: Validators with at least one unpaid epoch
- **Total Epochs**: Number of epochs being tracked (dynamically detected from CSV)
- **Total Debt**: Sum of all unpaid fees converted to USD

## Technical Details

- **Frontend**: Pure HTML, CSS, and JavaScript (no frameworks required)
- **Data Source**: GitHub raw CSV file
- **Currency Conversion**: Lamports to SOL (1 SOL = 1,000,000,000 lamports)
- **Responsive**: Mobile-friendly design with CSS Grid and Flexbox

## Browser Compatibility

- Chrome (recommended)
- Firefox
- Safari
- Edge

## Deployment

This is a static website that can be deployed to any web hosting service:
- GitHub Pages
- Netlify
- Vercel
- AWS S3
- Any web server

Simply upload the `index.html` file to your hosting service.

## Data Updates

The website automatically fetches the latest data from the GitHub repository each time it loads, ensuring you always see the most current fee payment status. The application dynamically detects new epochs as they're added to the CSV file, making it future-proof for the ongoing Solana epoch cycle (new epochs every ~2 days).

## Contributing

Feel free to submit issues or pull requests to improve the application.
