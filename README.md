# Game Day Notifications for San Antonio Spurs

### **Overview**
This project provides notifications for San Antonio Spurs game schedules. It retrieves real-time game information from a sports API and notifies users via their preferred method (email or SMS). The system is built using Python and integrates seamlessly with external APIs for sports data and notifications.

---

### **Features**
- **San Antonio Spurs Game Notifications**: Get alerts about upcoming Spurs games, including opponent, game time, and location.
- **Customizable Delivery Methods**: Receive notifications via email or SMS.
- **Real-Time Schedule Updates**: Automatically fetches game schedules from a reliable sports API.
- **Fan Engagement Features**: Adds optional game insights, player stats, and ticket information to notifications.

---

### **Technical Stack**
- **Language**: Python 3.x
- **APIs**:
  - Sports Data API (e.g., Sportsdata.io or ESPN API)
  - Notification Services (e.g., Twilio, SendGrid, AWS SES)
- **Core Libraries**:
  - `requests` - For API calls
  - `dotenv` - For managing environment variables
  - `smtplib` or `boto3` - For email notifications
  - `schedule` or `cron` - For scheduling notifications

---

### **Setup Instructions**

#### **1. Clone the Repository**
```bash
git clone https://github.com/ifeanyiro9/game-day-notifications.git
cd game-day-notifications
```

#### **2. Install Dependencies**
```bash
pip install -r requirements.txt
```

#### **3. Configure Environment Variables**
Create a `.env` file in the project root directory and include the following variables:
```env
SPORTS_API_KEY=your_sports_api_key
EMAIL_SERVICE_API_KEY=your_email_service_key
TEAM_NAME="San Antonio Spurs"
TIME_ZONE="America/Chicago"
NOTIFICATION_METHOD=email  # Choose email or SMS
```

#### **4. Set Up Notification Service**
- For **email notifications**, configure an SMTP server or a cloud email service (e.g., AWS SES or SendGrid).
- For **SMS notifications**, configure Twilio or another SMS provider.

#### **5. Run the Application**
```bash
python app.py
```

---

### **Usage**
1. **Fetch Game Schedule**:
   The script automatically retrieves the Spurs' game schedule for the week.
2. **Send Notifications**:
   Notifications will be sent to users based on the configured delivery method.
3. **Schedule Automation**:
   Use a task scheduler to send recurring notifications.

Example `cron` job:
```bash
0 9 * * * python /path/to/app.py  # Sends daily notifications at 9 AM
```

---

### **Project Structure**
```
game-day-notifications/
├── src/
│   ├── app.py               # Main application logic
│   ├── schedule_fetcher.py  # Script to fetch game schedules
│   ├── notifier.py          # Script to send notifications
├── requirements.txt         # Python dependencies
├── .env                     # Environment variables
├── README.md                # Project documentation
```

---

### **Customization**
- **Team Selection**:
  Modify the `TEAM_NAME` in the `.env` file to customize for another NBA team.
- **Notification Content**:
  Update `notifier.py` to include additional game information like stats or player highlights.
- **Time Zone Adjustments**:
  Ensure the `TIME_ZONE` variable matches the user's preferred time zone.

---

### **Future Enhancements**
- Add a web or mobile interface for user interaction.
- Integrate player stats and post-game analysis.
- Support multi-team notifications for broader NBA coverage.

---

### **License**
This project is licensed under the MIT License. See the `LICENSE` file for details.

---

### **Contact**
If you have questions or would like to contribute, feel free to reach out:
-**Author**: Carl Anthony Osborne
-**LinkedIn**: https://www.linkedin.com/in/carlanthonyosborne/
- **GitHub**: https://github.com/ehrconsultantforhire
-**eMail**: app@ehrconsultantforhire.com 
