# 🏋️‍♂️ SweatLogger

Welcome to **SweatLogger**, your personal workout sidekick! Tell it what you did, and it magically logs your exercises (with calories burned) into your workout spreadsheet. 💪✨

---

## 🎯 What It Does

1. **Asks** you “What exercises did you crush today?”  
2. **Talks** to the Nutritionix API to figure out what you did and how much energy you torched 🔥  
3. **Sends** your workout details (date, time, exercise, duration, calories) to your spreadsheet  
4. **Prints** the sheet’s response so you know it worked!

---

## 🚀 Getting Started

### 1. Clone the Repo
```bash
git clone https://github.com/yourusername/SweatLogger.git
cd SweatLogger
```

### 2. Install Dependencies
Make sure you have Python 3.x and `pip` installed:
```bash
pip install requests
```

### 3. Set Environment Variables
You'll need the following environment variables set up:

```bash
# Nutritionix credentials
export NT_APP_ID="your_nutritionix_app_id"
export NT_API_KEY="your_nutritionix_api_key"

# Your sheet endpoint (e.g., Google Apps Script Webhook)
export SHEET_ENDPOINT="https://your-sheet-endpoint.com"

# Bearer token for sheet API (if needed)
export TOKEN="your_bearer_token"
```

You can either export these in your terminal or use a `.env` file + `python-dotenv`.

### 4. Customize Your Profile
Edit the `main.py` and fill in your info:

```python
GENDER = "male"
WEIGHT_KG = "80"
HEIGHT_CM = "180"
AGE = "24"
```

---

## 🎉 How to Use

Run the script:

```bash
python main.py
```

It will ask:

```
Tell me which exercises you did:
```

Respond naturally:

```
Ran 3 miles and did 15 minutes of yoga
```

And BOOM 💥 — it gets logged to your spreadsheet!

---

## ❓ Troubleshooting

- ❌ **401/403 from Nutritionix?**  
  Double-check your `NT_APP_ID` and `NT_API_KEY`.

- 🧾 **Sheet not logging?**  
  Check your `SHEET_ENDPOINT` and make sure the Bearer `TOKEN` is valid.

- 🧠 **Weird results?**  
  Try to describe your exercises more clearly (e.g., "cycled 20 minutes" vs. "rode bike").

---

## 💡 Next Steps

- [ ] Add support for heart rate or distance metrics  
- [ ] Build a basic web interface  
- [ ] Get daily reminders and cron automation  
- [ ] Share logs to Slack, Discord, or Twitter 🚀

---

## 📬 Contributing

Want to help SweatLogger get swole? 💪

1. Fork it  
2. Create your feature branch (`git checkout -b feature/new-cool-thing`)  
3. Commit your changes (`git commit -m 'Add some cool feature'`)  
4. Push to the branch (`git push origin feature/new-cool-thing`)  
5. Open a Pull Request 🎉

---


