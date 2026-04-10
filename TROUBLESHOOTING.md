# 🔧 Troubleshooting Guide

## Common Issues

### 1. Bot not responding
**Symptom:** User sends message but gets no response
**Cause:** Make.com scenario is off
**Fix:** Go to Make.com → activate the scenario toggle

---

### 2. All tickets showing as Escalated
**Symptom:** Every ticket has Status = Escalated
**Cause:** Pinecone index is empty or API key expired
**Fix:**
1. Check Pinecone dashboard — verify vectors exist
2. Check Make.com scenario history for errors
3. Verify Anthropic API key is valid

---

### 3. Dashboard showing wrong numbers
**Symptom:** Looker Studio metrics don't match Airtable
**Cause:** Google Apps Script sync failed
**Fix:**
1. Open Google Sheets → Extensions → Apps Script
2. Run `syncAirtable` manually
3. Check execution log for errors

---

### 4. Slack notifications not arriving
**Symptom:** Escalated tickets not showing in Slack
**Cause:** Make.com escalation scenario is off or webhook expired
**Fix:**
1. Go to Make.com → Integration Airtable scenario
2. Verify toggle is ON
3. Check scenario history for errors

---

### 5. Google Apps Script daily errors
**Symptom:** Daily failure emails from Apps Script
**Cause:** Trigger permissions expired
**Fix:**
1. Open Apps Script → Triggers (clock icon)
2. Delete existing trigger
3. Create new trigger → re-authorize permissions

---

## Support
For additional help contact: [tu email]
