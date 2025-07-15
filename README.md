# 🚌 Bus Operator Glide App — Setup Guide

## 📦 Data Tables

### 1. Users
| Name      | Email      | Role   | Staff ID   |
|-----------|------------|--------|------------|
| Text      | Email      | Text   | Text       |
| (Full Name) | (Login)  | admin/staff | Optional  |

- **Settings:** Go to Glide > Settings > User Profiles → select Users table.
- **Visibility:**  
  - Staff: Booking & Expense screens  
  - Admin: Reports screen

---

### 2. Bookings
| Passenger Name | From  | To    | Seat No | Fare | Photo | Location | Time | Booked By | Locked |
|----------------|-------|-------|---------|------|-------|----------|------|-----------|--------|
| Text           | Choice/Text | Choice/Text | Number  | Number | Image | Location | Date/Time | Email | Boolean |

- **Form Button:** `New Booking`
- **Auto-Fill:**  
  - Date/Time: current time  
  - Location: device GPS  
  - Booked By: logged-in user  
- **Lock:** Set Locked = TRUE after submission

---

### 3. Expenses
| Expense Type | Amount | Description | Photo | Location | Time | Staff |
|--------------|--------|-------------|-------|----------|------|-------|
| Choice       | Number | Text        | Image | Location | Date/Time | Email |

- **Form Button:** `Add Expense`
- **Auto-Fill:**  
  - Time: current time  
  - Location: GPS  
  - Staff: logged-in user

---

## 🖼️ Logo
- Upload to Glide branding or use image URL.
- Display at top of Booking form, Receipt view, Admin screen.

---

## 🧾 Formatted Bill Screen (Booking/Expense)
- Logo (image)
- Title (“Passenger Receipt” or “Expense Receipt”)
- All fields from booking/expense
- Time & Location
- Staff Name
- **Button:** Print / Share Bill (share link or copy screen)

**Optional PDF:**
- Use Zapier or Make.com to create and send PDF receipts.

---

## 📊 Admin Report Screen
- **Filters:** Date range, Staff, Booking/Expenses
- **Display:**  
  - Total fares  
  - Total expenses  
  - Net profit (via math column)
- **Export:**  
  - Enable Download as CSV in Glide

---

## 🔒 Booking Lock
- On submit: set Locked = TRUE
- On edit: Show edit button only if Locked = FALSE

---

## 📍 GPS & Time—How to Set
- **Location:** “Location” component
- **Time:** “Date/Time” → “Now”
- **Staff:** logged-in user profile

---

## ✅ Deliverables Checklist
| Feature                   | Type              | Complete? |
|---------------------------|-------------------|-----------|
| Staff login               | User Profiles     | ✅        |
| Passenger booking         | Form screen       | ✅        |
| Trip expense entry        | Form screen       | ✅        |
| Auto time & location      | Form fields       | ✅        |
| Photo upload              | Form fields       | ✅        |
| Admin report              | Filtered list     | ✅        |
| Locked bookings           | Boolean logic     | ✅        |
| Bill with logo            | Detail screen/PDF | ✅        |
| Export to Excel           | CSV export        | ✅        |

---

## 🚀 Setup Steps

1. **Create Tables:** Users, Bookings, Expenses.
2. **Set User Profiles** in Glide using Users table.
3. **Build Forms:**  
   - Booking Form (auto time, location, photo, lock after submit)  
   - Expense Form (auto time, location, photo, notes)
4. **Detail Screens:**  
   - Booking/Expense receipts with logo, print/share button.
5. **Admin Screen:**  
   - Filter, chart, export options for reports.
6. **Permissions:**  
   - Set visibility for staff/admin.
7. **Lock Logic:**  
   - Prevent editing locked bookings.
8. **Branding:**  
   - Add your logo to top of screens.
9. **Export:**  
   - Enable CSV export as needed.

---

## 💡 Tips

- **Form Buttons:** Use “New Booking” and “Add Expense” for clarity.
- **Location & Time:** Always use auto-capture for accuracy.
- **User Roles:** Ensure visibility rules are correct for staff/admin access.
- **PDF/Print:** Use Zapier/Make integration for advanced receipts.
