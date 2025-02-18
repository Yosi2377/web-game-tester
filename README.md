# Web Game Tester 🎮

[English](#english) | [עברית](#hebrew)

<a name="english"></a>
## English

An automated testing tool for web-based games. This tool provides a flexible framework for testing various aspects of browser-based games, including user interactions, timing, state transitions, and performance monitoring.

### ✨ Key Features

- ⚙️ JSON-configurable test scenarios
- 🔑 Automated authentication and login
- ⏱️ Game event timing verification
- 📊 State monitoring and assertions
- 📈 Performance metrics collection
- 🚨 Comprehensive error logging
- 📝 Customizable reporting

### 🚀 Installation

#### Global Installation
```bash
npm install -g https://github.com/Yosi2377/web-game-tester.git
```

#### Project Installation
```bash
# As a development dependency
npm install --save-dev https://github.com/Yosi2377/web-game-tester.git

# Or as a regular dependency
npm install https://github.com/Yosi2377/web-game-tester.git
```

### 📋 Usage

#### Configuration File Setup
Create a `test-config.json`:

```json
{
  "baseUrl": "http://your-game-url",
  "timeout": 30000,
  "viewport": {
    "width": 1280,
    "height": 720
  },
  "auth": {
    "enabled": true,
    "selectors": {
      "username": "input[type='text']",
      "password": "input[type='password']",
      "submit": "button[type='submit']"
    },
    "credentials": {
      "username": "your-username",
      "password": "your-password"
    }
  },
  "gameActions": {
    "join": {
      "selector": "button:has-text('JOIN')",
      "timeout": 5000
    },
    "actions": [
      {
        "name": "action1",
        "selector": "button.action1",
        "timeout": 2000
      }
    ]
  }
}
```

#### Running Tests

```bash
# Run with config file
game-test --config ./test-config.json

# Run with custom URL
game-test --url http://your-game-url
```

### ⚙️ Configuration Options

#### Base Configuration
```json
{
  "baseUrl": "Game URL",
  "timeout": "Global timeout in ms",
  "viewport": {
    "width": "Browser width",
    "height": "Browser height"
  }
}
```

#### Authentication
```json
{
  "auth": {
    "enabled": true,
    "selectors": {
      "username": "CSS selector for username field",
      "password": "CSS selector for password field",
      "submit": "CSS selector for submit button"
    },
    "credentials": {
      "username": "Username",
      "password": "Password"
    }
  }
}
```

#### Game Actions
```json
{
  "gameActions": {
    "join": {
      "selector": "Join button selector",
      "timeout": "Timeout in ms"
    },
    "actions": [
      {
        "name": "Action name",
        "selector": "Button selector",
        "timeout": "Timeout in ms"
      }
    ]
  }
}
```

#### Monitoring
```json
{
  "monitoring": {
    "console": {
      "enabled": true,
      "levels": ["error", "warning", "info", "log"]
    },
    "network": {
      "enabled": true,
      "failedRequestsOnly": false
    },
    "performance": {
      "enabled": true,
      "metrics": ["FPS", "Memory", "CPU"]
    }
  }
}
```

### 📊 Sample Test Report

```json
{
  "duration": 15000,
  "tests": {
    "total": 10,
    "passed": 9,
    "failed": 1
  },
  "performance": {
    "avgFPS": 60,
    "memoryUsage": "150MB",
    "cpuUsage": "25%"
  },
  "errors": [
    {
      "type": "timing",
      "message": "Bot response time exceeded maximum delay",
      "timestamp": "2024-03-14T12:00:00Z"
    }
  ]
}
```

### 🛠️ Development

To add new features or modify existing ones:

1. Install development dependencies:
```bash
npm install
```

2. Edit code in `src/`:
   - `core/` - Core logic
   - `utils/` - Helper functions
   - `types/` - Type definitions

3. Build and test:
```bash
npm run build
npm test
```

### 🤝 Contributing

1. Fork the project
2. Create your feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

### 📝 License

ISC

---

<a name="hebrew"></a>
## עברית

כלי אוטומטי לבדיקת משחקי דפדפן. הכלי מספק מסגרת גמישה לבדיקת היבטים שונים של משחקים מבוססי דפדפן, כולל אינטראקציות משתמש, תזמון, מעברי מצב וניטור ביצועים.

### ✨ תכונות עיקריות

- ⚙️ תרחישי בדיקה הניתנים להגדרה באמצעות JSON
- 🔑 אימות והתחברות אוטומטיים
- ⏱️ אימות תזמון לאירועי משחק
- 📊 ניטור מצב ובדיקות
- 📈 איסוף מדדי ביצועים
- 🚨 תיעוד שגיאות מקיף
- 📝 דוחות מותאמים אישית

### 🚀 התקנה

#### התקנה גלובלית
```bash
npm install -g https://github.com/Yosi2377/web-game-tester.git
```

#### התקנה בפרויקט
```bash
# התקנה כתלות פיתוח
npm install --save-dev https://github.com/Yosi2377/web-game-tester.git

# או כתלות רגילה
npm install https://github.com/Yosi2377/web-game-tester.git
```

### 📋 שימוש

#### הגדרת קובץ קונפיגורציה
צור קובץ `test-config.json`:

```json
{
  "baseUrl": "http://your-game-url",
  "timeout": 30000,
  "viewport": {
    "width": 1280,
    "height": 720
  },
  "auth": {
    "enabled": true,
    "selectors": {
      "username": "input[type='text']",
      "password": "input[type='password']",
      "submit": "button[type='submit']"
    },
    "credentials": {
      "username": "your-username",
      "password": "your-password"
    }
  },
  "gameActions": {
    "join": {
      "selector": "button:has-text('JOIN')",
      "timeout": 5000
    },
    "actions": [
      {
        "name": "action1",
        "selector": "button.action1",
        "timeout": 2000
      }
    ]
  }
}
```

#### הרצת בדיקות

```bash
# הרצה עם קובץ קונפיגורציה
game-test --config ./test-config.json

# הרצה עם כתובת URL מותאמת
game-test --url http://your-game-url
```

### ⚙️ אפשרויות קונפיגורציה

#### הגדרות בסיס
```json
{
  "baseUrl": "כתובת המשחק",
  "timeout": "טיימאאוט גלובלי במילישניות",
  "viewport": {
    "width": "רוחב הדפדפן",
    "height": "גובה הדפדפן"
  }
}
```

#### אימות
```json
{
  "auth": {
    "enabled": true,
    "selectors": {
      "username": "סלקטור CSS לשדה שם משתמש",
      "password": "סלקטור CSS לשדה סיסמה",
      "submit": "סלקטור CSS לכפתור שליחה"
    },
    "credentials": {
      "username": "שם משתמש",
      "password": "סיסמה"
    }
  }
}
```

#### פעולות משחק
```json
{
  "gameActions": {
    "join": {
      "selector": "סלקטור לכפתור הצטרפות",
      "timeout": "טיימאאוט במילישניות"
    },
    "actions": [
      {
        "name": "שם הפעולה",
        "selector": "סלקטור לכפתור",
        "timeout": "טיימאאוט במילישניות"
      }
    ]
  }
}
```

### 🛠️ פיתוח

להוספת תכונות חדשות או שינוי קיימות:

1. התקן את תלויות הפיתוח:
```bash
npm install
```

2. ערוך את הקוד ב-`src/`:
   - `core/` - לוגיקה מרכזית
   - `utils/` - פונקציות עזר
   - `types/` - הגדרות טיפוסים

3. בנה ובדוק:
```bash
npm run build
npm test
```

### 🤝 תרומה לפרויקט

1. בצע Fork לפרויקט
2. צור ענף חדש לתכונה שלך
3. בצע Commit לשינויים
4. דחוף לענף
5. פתח Pull Request

### 📝 רישיון

ISC 