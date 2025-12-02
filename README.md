# Hostel Management System

A web and mobile platform for managing hostel operations for 60,000 students.

## 📋 Project Requirements

### Target Users
- **Total Students:** 60,000
- **Platform:** Primarily mobile (web + mobile app)
- **User Types:** Students, Admins, Super Admin (CRUD for admins)

### Core Features

#### 1. User Authentication & Onboarding
- Student registration with email and phone number
- OTP verification for phone number
- Hostel verification process
  - Students upload hostel ID card/proof
  - Admins manually verify and approve/reject
- Multi-admin support for verification

#### 2. Attendance Tracking
- QR code-based attendance marking
- Daily attendance records
- Monthly attendance history
- Attendance reports for admins
- Analytics dashboard showing attendance trends

#### 3. Event Management
- Event creation by admins
  - Event details (title, description, date, images)
  - Maximum participant limits
  - Registration deadlines
- Student event registration
  - Browse upcoming events
  - Register/unregister for events
  - View registration status
- Event leaderboards
  - Display rankings/winners
  - Prize information
  - Winner announcements by admins

#### 4. Announcements & Notifications
- Admin can create announcements
  - Title, body, images
  - Priority levels (Low, Medium, High, Urgent)
  - Target specific audiences (All, Students, Admins)
- Push notifications to mobile devices
- In-app announcement feed
- Mark announcements as read/unread

#### 5. Admin Dashboard
- User statistics (total users, active users)
- Attendance statistics
- Event participation metrics
- Pending approval requests
- User management (view, suspend, activate)

#### 6. User Profile Management
- View and edit profile information
- Upload profile picture
- Update room number and hostel details
- Notification preferences

- #### 9. Search & Filters
- Search events by name/date
- Filter announcements by priority
- Search users (admin only)

### Additional Features (Nice to Have)

#### 7. Mess Menu Management
- Weekly/daily mess menu
- Meal timings
- Special meal announcements

#### 8. Complaint/Request System
- Students can raise complaints
- Ticket status tracking
- Admin can respond and resolve


## 🎯 User Flows

### Student Flow
1. Register with email + phone → Verify OTP
2. Upload hostel ID proof → Wait for admin approval
3. Get approved → Access app
4. Mark daily attendance via QR code
5. Browse and register for events
6. View announcements and notifications
7. Check attendance history and event registrations

### Admin Flow
1. Login to admin panel
2. Review pending student approvals (view ID proof)
3. Approve/reject student registrations
4. Create and manage events
5. Add event winners and prizes
6. Create announcements for students
7. View attendance and event reports
8. Manage user accounts

## 📊 Functional Requirements

### Attendance System
- Students can mark attendance once per day
- QR code expires after specific time period
- Geolocation verification (optional)
- Cannot mark attendance for past dates
- Attendance status: Present, Absent, Late

### Event System
- Registration closes when max capacity reached
- Cannot register after deadline
- Cannot register for past events
- Email/push notification on successful registration
- Cannot register for conflicting events (optional)

### Notification System
- Real-time push notifications
- Notification history
- Different notification types (event, announcement, approval)
- Notification preferences (enable/disable)

### Admin Controls
- Multiple admins with same privileges
- Super admin can manage other admins
- Audit logs for admin actions
- Bulk operations (approve multiple users)

## 🔒 Security & Privacy Requirements

- Secure authentication (OTP + password)
- Password encryption
- Phone number hashing (for privacy)
- Role-based access control (Student, Admin, Super Admin)
- API rate limiting
- Secure file upload (ID proofs, images)
- HTTPS only

## 📝 Assumptions

1. Students have smartphones with camera
2. Internet connectivity is available 
3. Students have valid email and phone number
4. QR codes for attendance will be generated and displayed by admins
5. One student belongs to one hostel only
6. Events are hostel-specific

## 🚫 Out of Scope (Not Required)

- Payment processing
- Chat/messaging between users
- Video streaming
- Advanced analytics with ML
- Mobile native apps (using PWA instead)
- Multi-language support (English only for now)
- Email notifications (push notifications only)

---

**Document Version:** 1.0  
**Last Updated:** December 2025
**Status:** Ready for Review by Timy
