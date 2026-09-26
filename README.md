# Excellence Academy - School Management System

A comprehensive school management system built with React, Vite, and Tailwind CSS. Features student tracking, XP-based gamification, rankings, events, sports competitions, and a full admin panel.

## 🚀 Features

### Phase 1: Foundation
- ✅ React + Vite setup with professional folder structure
- ✅ Tailwind CSS with custom dark theme
- ✅ React Router for navigation
- ✅ Reusable UI components (Button, Input, Card, Badge, Modal, Toast, Avatar)
- ✅ Theme system with dark/light mode
- ✅ LocalStorage abstraction layer
- ✅ API-ready service architecture
- ✅ Comprehensive mock data

### Phase 2: Authentication
- ✅ Login with role-based access
- ✅ Registration system
- ✅ Logout functionality
- ✅ Remember me feature
- ✅ Role management (Student, Teacher, Class Teacher, Admin)
- ✅ Demo authentication via localStorage

### Phase 3: Student System
- ✅ Dashboard with statistics and progress
- ✅ Profile management
- ✅ Activities tracking with XP rewards
- ✅ Achievements and badges
- ✅ Certificates management
- ✅ Projects portfolio
- ✅ Events participation
- ✅ Announcements
- ✅ XP history and level progression
- ✅ Statistics and timeline

### Phase 4: Ranking System
- ✅ School-wide rankings
- ✅ Class rankings
- ✅ Category-based rankings (Academic, Sports, Technology, Creativity)
- ✅ Top 3 podium display
- ✅ Filterable leaderboards

### Phase 5: Admin Panel
- ✅ User management (CRUD)
- ✅ Class management
- ✅ Activity management
- ✅ Event management
- ✅ Settings configuration
- ✅ Role-based access control

### Phase 6: Events & Announcements
- ✅ Event creation and management
- ✅ Event participation (join/leave)
- ✅ Audience targeting
- ✅ Event status tracking
- ✅ XP rewards for events
- ✅ Announcements with priority levels
- ✅ Target audience filtering

### Phase 7: Sports System
- ✅ Multiple sports categories (Football, Basketball, Chess, etc.)
- ✅ Team sports with standings
- ✅ Individual sports with rankings
- ✅ Match tracking
- ✅ MVP system
- ✅ Score management

### Phase 8: Analytics
- ✅ Student performance charts
- ✅ XP trend analysis
- ✅ Category distribution
- ✅ Activity statistics
- ✅ Recharts integration

### Phase 9: UX Features
- ✅ Dark/light mode toggle
- ✅ Responsive design (desktop/tablet/mobile)
- ✅ Glassmorphism UI design
- ✅ Smooth animations
- ✅ Modal dialogs
- ✅ Toast notifications
- ✅ Loading states
- ✅ Empty states
- ✅ Professional typography

## 📋 Demo Accounts

Use these accounts to test different roles:

| Role | Email | Password |
|------|-------|----------|
| Admin | admin@school.com | admin123 |
| Teacher | teacher@school.com | teacher123 |
| Class Teacher | classteacher@school.com | classteacher123 |
| Student | student@school.com | student123 |
| Student 2 | student2@school.com | student123 |

## 🛠️ Installation

### Prerequisites
- Node.js (v18 or higher)
- npm or yarn

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd WebSite
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Run development server**
   ```bash
   npm run dev
   ```

4. **Build for production**
   ```bash
   npm run build
   ```

5. **Preview production build**
   ```bash
   npm run preview
   ```

## 🏗️ Architecture

### Project Structure

```
WebSite/
├── src/
│   ├── components/
│   │   ├── ui/              # Reusable UI components
│   │   │   ├── Button.jsx
│   │   │   ├── Input.jsx
│   │   │   ├── Card.jsx
│   │   │   ├── Badge.jsx
│   │   │   ├── Modal.jsx
│   │   │   ├── Toast.jsx
│   │   │   └── Avatar.jsx
│   │   ├── layout/          # Layout components
│   │   │   ├── Navbar.jsx
│   │   │   └── Sidebar.jsx
│   │   ├── auth/            # Authentication components
│   │   ├── student/         # Student-specific components
│   │   ├── admin/           # Admin-specific components
│   │   ├── ranking/         # Ranking components
│   │   ├── events/          # Event components
│   │   └── sports/          # Sports components
│   ├── contexts/            # React contexts
│   │   ├── AuthContext.jsx
│   │   └── ThemeContext.jsx
│   ├── services/            # API services
│   │   └── authService.js
│   ├── hooks/               # Custom hooks
│   ├── utils/               # Utility functions
│   │   └── localStorage.js
│   ├── data/                # Mock data
│   │   └── mockData.js
│   ├── pages/               # Page components
│   │   ├── Login.jsx
│   │   ├── Register.jsx
│   │   ├── Dashboard.jsx
│   │   ├── Profile.jsx
│   │   ├── Activities.jsx
│   │   ├── Achievements.jsx
│   │   ├── Certificates.jsx
│   │   ├── Projects.jsx
│   │   ├── Rankings.jsx
│   │   ├── Events.jsx
│   │   ├── Announcements.jsx
│   │   ├── Sports.jsx
│   │   ├── Analytics.jsx
│   │   ├── Admin.jsx
│   │   └── Settings.jsx
│   ├── styles/              # Global styles
│   ├── App.jsx              # Main app component
│   └── index.css            # Global CSS
├── public/                  # Static assets
├── .env.example             # Environment variables template
├── .gitignore              # Git ignore rules
├── tailwind.config.js      # Tailwind configuration
├── postcss.config.js       # PostCSS configuration
├── vite.config.js          # Vite configuration
└── package.json            # Dependencies and scripts
```

### Key Architectural Decisions

1. **Service Layer Pattern**
   - All data operations go through service functions
   - Easy to replace localStorage with REST API
   - Consistent error handling
   - Mock data for development

2. **Context API for State Management**
   - AuthContext for user authentication
   - ThemeContext for UI theming
   - Lightweight alternative to Redux

3. **Component Composition**
   - Reusable UI components in `/components/ui`
   - Layout components for structure
   - Feature-specific components organized by domain

4. **LocalStorage Abstraction**
   - Centralized storage interface
   - Type-safe operations
   - Easy migration to backend storage

5. **Role-Based Access Control**
   - Middleware-style route protection
   - Component-level role checks
   - Admin-only sections

### Data Model

The system uses interconnected data:

- **Users**: Students, teachers, class teachers, admins
- **Classes**: Student groups with class teachers
- **Activities**: Student actions earning XP
- **Achievements**: Badges and accomplishments
- **Certificates**: Official credentials
- **Projects**: Portfolio work
- **Events**: School activities with participation
- **Announcements**: School communications
- **Sports**: Competition data and standings
- **Settings**: System configuration

All data is currently stored in localStorage with mock data for demonstration.

## 🔧 Configuration

### Environment Variables

Create a `.env` file based on `.env.example`:

```env
VITE_API_URL=http://localhost:3000/api
VITE_API_KEY=your_api_key_here
VITE_ENABLE_ANALYTICS=true
VITE_ENABLE_NOTIFICATIONS=true
VITE_ENVIRONMENT=development
```

### Tailwind Configuration

Custom theme defined in `tailwind.config.js`:
- Custom color palette
- Dark mode support
- Glassmorphism utilities
- Responsive breakpoints

## 🎨 Design System

### Colors
- Primary: Purple gradient
- Background: Dark futuristic theme
- Accent: Pink/Purple highlights
- Success/Error states with semantic colors

### Typography
- System fonts for performance
- Clear hierarchy
- Accessible contrast ratios

### Components
- Glassmorphism cards
- Smooth transitions
- Hover effects
- Loading states
- Empty states

## 🚀 Deployment

### Production Build

```bash
npm run build
```

The build output will be in the `dist/` directory.

### Deployment Options

1. **Netlify**
   - Connect your repository
   - Build command: `npm run build`
   - Publish directory: `dist`

2. **Vercel**
   - Import your repository
   - Framework preset: Vite
   - Build command: `npm run build`
   - Output directory: `dist`

3. **Traditional Hosting**
   - Build the project
   - Upload `dist/` contents to your server
   - Configure server to handle SPA routing

## 🔐 Security Considerations

- Passwords are stored in plaintext (demo only)
- No real authentication backend
- localStorage is not secure for sensitive data
- CSRF protection not implemented
- Input validation should be enhanced

**For production use:**
- Implement proper backend authentication
- Use HTTPS
- Add CSRF protection
- Implement proper session management
- Add rate limiting
- Validate and sanitize all inputs

## 📝 Future Enhancements

- [ ] Real backend API integration
- [ ] Real-time notifications
- [ ] File upload for projects/certificates
- [ ] Advanced analytics
- [ ] Mobile app (React Native)
- [ ] Parent portal
- [ ] Gradebook integration
- [ ] Attendance tracking
- [ ] Fee management
- [ ] Library management

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License.

## 🙏 Acknowledgments

- Built with React and Vite
- UI components inspired by modern SaaS designs
- Icons from Lucide React
- Charts from Recharts
- Styling with Tailwind CSS

## 📞 Support

For support and questions, please open an issue in the repository.

---

**Excellence Academy v1.0** - Built with ❤️ for education