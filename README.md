# ClinicAppointmentSystem

Generated ERD <img width="1953" height="811" alt="clinic_erd" src="https://github.com/user-attachments/assets/69efebf5-2449-4a34-a7e1-e9af32b319c5" />

## Cron Configuration & Management Commands

### Daily Appointment Reminders
To send automatic email and in-app appointment reminders, run the following management command:
```bash
python manage.py send_reminders
```

You can test the command without sending actual emails or writing notifications to the database by using the `--dry-run` flag:
```bash
python manage.py send_reminders --dry-run
```

### Cron Setup
To schedule the reminders automatically every day at 6:00 PM (before the next day's scheduled appointments), add the following cron job to your server:

```cron
# Run at 6 PM daily (before next day's appointments)
0 18 * * * cd /path/to/project && /path/to/venv/bin/python manage.py send_reminders >> /var/log/clinic_reminders.log 2>&1
```
