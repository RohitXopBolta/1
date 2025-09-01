# Braintree Bot

A Telegram bot for Braintree payment processing.

## Deployment on Render

### Step 1: Prepare Your Repository
1. Make sure all your files are committed to a Git repository (GitHub, GitLab, etc.)
2. Ensure you have the following files in your repository:
   - `main.py` (your main bot file)
   - `requirements.txt` (dependencies)
   - `render.yaml` (deployment configuration)
   - `runtime.txt` (Python version)
   - `Procfile` (start command)

### Step 2: Deploy on Render
1. Go to [render.com](https://render.com) and create an account
2. Click "New +" and select "Web Service"
3. Connect your Git repository
4. Configure the service:
   - **Name**: `braintree-bot` (or any name you prefer)
   - **Environment**: `Python 3`
   - **Build Command**: `pip install -r requirements.txt`
   - **Start Command**: `python main.py`
   - **Plan**: Free (or choose paid plan if needed)

### Step 3: Environment Variables (Optional)
If your bot uses environment variables, add them in the Render dashboard:
- Go to your service settings
- Navigate to "Environment" tab
- Add any required environment variables

### Step 4: Deploy
1. Click "Create Web Service"
2. Render will automatically build and deploy your bot
3. Monitor the build logs for any errors
4. Once deployed, your bot will be running 24/7

## Important Notes

- **Free Plan Limitations**: Render's free plan has limitations:
  - Service sleeps after 15 minutes of inactivity
  - Limited bandwidth and build minutes
  - Consider upgrading for production use

- **Bot Token**: Make sure your Telegram bot token is properly configured in your code

- **Keep Alive**: The bot includes a Flask web server for keep-alive functionality

## Files Structure
```
├── main.py              # Main bot file
├── GATEAU.py            # Braintree processing module
├── hh.py                # Keep alive module
├── requirements.txt     # Python dependencies
├── render.yaml          # Render deployment config
├── runtime.txt          # Python version
├── Procfile            # Start command
└── README.md           # This file
```

## Troubleshooting

1. **Build Failures**: Check the build logs in Render dashboard
2. **Import Errors**: Ensure all dependencies are in `requirements.txt`
3. **Bot Not Responding**: Verify your bot token and webhook settings
4. **Service Sleeping**: Free plan services sleep after inactivity

## Support

For issues with:
- **Render Deployment**: Check Render documentation
- **Bot Functionality**: Review your bot code and Telegram API documentation
