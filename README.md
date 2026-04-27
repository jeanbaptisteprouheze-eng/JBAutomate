# JBAutomate

A comprehensive personal automation platform to streamline everyday tasks including financial management, meal planning, and travel organization.

## 🎯 Features

### 📊 Financial Automation
- **Bank Statement Extraction**: Automatically parse and extract data from bank statements
- **Budget Tracking**: Real-time budget updates and expense categorization
- **Financial Reports**: Generate monthly/quarterly financial summaries

### 🍽️ Meal Planning
- **Family Meal Planning**: Collaborative meal planning for the entire family
- **Recipe Management**: Organize and categorize recipes
- **Grocery List Generation**: Automatic grocery lists based on planned meals
- **Dietary Preferences**: Track allergies and dietary restrictions

### ✈️ Travel Planning
- **Itinerary Management**: Organize trips and activities
- **Cost Tracking**: Monitor travel expenses
- **Document Management**: Store confirmations and travel documents
- **Notifications**: Reminders for flights, bookings, and reservations

## 🚀 Quick Start

### Prerequisites
- Python 3.8+
- pip (Python package installer)
- Git

### Installation

**Windows:**
```cmd
git clone https://github.com/jeanbaptisteprouheze-eng/JBAutomate.git
cd JBAutomate
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
```

**macOS/Linux:**
```bash
git clone https://github.com/jeanbaptisteprouheze-eng/JBAutomate.git
cd JBAutomate
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

### Configuration

1. Copy `.env.example` to `.env`
2. Update `.env` with your personal settings
3. Run initialization: `python -m jbautomate init`

## 📁 Project Structure

```
JBAutomate/
├── jbautomate/
│   ├── __init__.py
│   ├── finance/              # Bank statement extraction & budgeting
│   │   ├── __init__.py
│   │   ├── extractors.py
│   │   └── budget.py
│   ├── meals/                # Meal planning & recipes
│   │   ├── __init__.py
│   │   ├── planner.py
│   │   └── recipes.py
│   ├── travel/               # Travel planning & itineraries
│   │   ├── __init__.py
│   │   ├── planner.py
│   │   └── itinerary.py
│   └── core/                 # Shared utilities
│       ├── __init__.py
│       ├── config.py
│       └── logger.py
├── tests/
├── docs/
├── .env.example
├── requirements.txt
├── setup.py
└── README.md
```

## 🔧 Development

### Running Tests
```bash
pytest tests/
```

### Code Style
This project uses `black` and `flake8` for code formatting.

```bash
black jbautomate/
flake8 jbautomate/
```

## 📖 Documentation

- [Financial Automation Guide](docs/finance.md)
- [Meal Planning Guide](docs/meals.md)
- [Travel Planning Guide](docs/travel.md)
- [API Reference](docs/api.md)

## 🤝 Contributing

Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on how to contribute to this project.

## 📝 License

This project is licensed under the MIT License - see [LICENSE](LICENSE) file for details.

## ⚠️ Security & Privacy

This tool handles sensitive personal and financial data. Please:
- Never commit `.env` files or sensitive credentials
- Use environment variables for all secrets
- Enable file encryption for local data storage
- Review security practices in [docs/security.md](docs/security.md)

## 💡 Roadmap

- [ ] Web UI for non-technical users
- [ ] Mobile app integration
- [ ] Cloud synchronization
- [ ] AI-powered expense categorization
- [ ] Integration with banking APIs
- [ ] Calendar sync for travel events

## 📧 Support

For issues, questions, or suggestions, please open an [issue](https://github.com/jeanbaptisteprouheze-eng/JBAutomate/issues).

---

**Last Updated:** 2026-04-27
