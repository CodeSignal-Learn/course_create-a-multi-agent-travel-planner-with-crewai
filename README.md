# Create a Multi-Agent Travel Planner with Crewai and Flask

This project demonstrates how to build an intelligent travel planning application using Flask (Python web framework) and CrewAI. The application uses AI agents to research destinations and create personalized travel itineraries.

## Features

- Interactive web-based travel planning interface
- AI-powered destination research and itinerary planning
- Real-time web search integration using DuckDuckGo
- Website scraping capabilities for up-to-date information
- Detailed daily itineraries with attractions and meal suggestions
- Cultural insights and local tips
- Clean and responsive user interface

## Prerequisites

- Python 3.10 or higher
- pip (Python package installer)
- OpenAI API access

## Installation

1. Clone the repository:
```bash
git clone https://github.com/CodeSignal-Learn/course_create-a-multi-agent-travel-planner-with-crewai-and-flask
cd course_create-a-multi-agent-travel-planner-with-crewai-and-flask
```

2. Install the required dependencies:
```bash
pip install -r requirements.txt
```

## Configuration

Before running the application, you need to set up your OpenAI API key. You can do this by exporting it as an environment variable:

For macOS/Linux:
```bash
export OPENAI_API_KEY='your-api-key-here'
```

For Windows (Command Prompt):
```cmd
set OPENAI_API_KEY=your-api-key-here
```

For Windows (PowerShell):
```powershell
$env:OPENAI_API_KEY='your-api-key-here'
```

## Running the Application

1. Start the Flask development server:
```bash
cd app
python main.py
```

2. Open your web browser and navigate to:
```
http://localhost:3000
```

## Usage

1. Enter the city you want to visit
2. Specify the number of days for your trip
3. Choose how many attractions you'd like to visit per day
4. Click "Plan Trip" to generate your personalized itinerary
5. View your detailed travel plan, including:
   - Daily attraction schedules
   - Transportation recommendations
   - Meal suggestions
   - Cultural insights and tips

## Project Structure

```
.
├── README.md
├── requirements.txt
├── startup.py
└── app/
    ├── main.py                 # Main Flask application
    ├── static/                 # Static files (CSS, JS)
    │   └── js/
    │       └── travel-planner.js
    ├── templates/              # HTML templates
    │   └── index.html
    └── travel_planner/         # Core travel planning logic
        ├── travel_planner_crew.py  # CrewAI implementation
        ├── models/             # Data models
        │   ├── travel_itinerary.py
        │   ├── daily_plan.py
        │   └── attraction.py
        ├── tools/             # Custom tools
        │   └── custom_search_tool.py
        └── config/            # Configuration files
            ├── agents.yaml
            └── tasks.yaml
```

The project follows a modular architecture:
- `main.py`: Handles web routes and request processing
- `travel_planner_crew.py`: Implements the AI agents and their tasks
- Models: Define the data structures for itineraries and attractions
- Tools: Provide custom functionality for web search and scraping
- Config: Contains YAML configurations for agents and tasks
- Static/Templates: Handle the frontend presentation