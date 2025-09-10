# AgentsVille Trip Planner 🏙️✈️

An advanced AI-powered travel planning system that demonstrates cutting-edge LLM reasoning techniques including role-based prompting, chain-of-thought reasoning, ReAct prompting, and feedback loops.

## 🎯 Project Overview

This project implements an intelligent travel agent that plans the perfect vacation to the wonderful city of AgentsVille! The system uses multiple AI agents and sophisticated reasoning patterns to create personalized, weather-aware itineraries that satisfy traveler preferences and constraints.

## 🚀 Key Features

### Advanced AI Techniques Demonstrated
- **Role-Based Prompting**: Specialized AI agents act as expert travel planners
- **Chain-of-Thought Reasoning**: Step-by-step itinerary planning process
- **ReAct Prompting**: Thought → Action → Observation cycles for iterative improvement
- **Feedback Loops**: Self-evaluation and plan refinement capabilities

### Intelligent Planning Capabilities
- 🌤️ **Weather-Aware Planning**: Automatically avoids outdoor activities during bad weather
- 💰 **Budget Management**: Keeps total costs within specified budget constraints
- 🎯 **Interest Matching**: Selects activities based on traveler preferences
- 📅 **Multi-Day Itineraries**: Plans detailed day-by-day schedules
- 🔄 **Iterative Refinement**: Uses evaluation functions to improve plans

## 📋 Project Structure

### Core Components

1. **VacationInfo System** (`project_starter.ipynb` cells 5-7)
   - Pydantic models for structured vacation data
   - Traveler profiles with interests and preferences
   - Date and budget constraints

2. **ItineraryAgent** (`project_starter.ipynb` cells 12-14)
   - Initial itinerary generation using Chain-of-Thought prompting
   - Weather and activity data integration
   - Structured output generation

3. **Evaluation Framework** (`project_starter.ipynb` cells 16-22)
   - Comprehensive evaluation functions
   - Date validation, budget checking, interest satisfaction
   - Weather compatibility assessment using LLM evaluation

4. **Tool System** (`project_starter.ipynb` cells 25-30)
   - Calculator tool for accurate cost calculations
   - Activity lookup tools for real-time data
   - Evaluation runner for quality assessment
   - Final answer tool for structured output

5. **ItineraryRevisionAgent** (`project_starter.ipynb` cells 32-37)
   - ReAct-based iterative improvement
   - Tool-assisted plan refinement
   - Weather compatibility fixes

## 🛠️ Setup and Installation

### Prerequisites
- Python 3.8+
- OpenAI API access (or Vocareum endpoint)
- Required Python packages (see `pyproject.toml`)

### Environment Setup
1. Clone this repository
2. Create a `.env` file with your OpenAI API key:
   ```
   OPENAI_API_KEY=your_api_key_here
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## 📖 Usage Guide

### Running the Notebook

1. **Setup Phase** (Cells 1-4):
   - Configure OpenAI client and model selection
   - Set vacation parameters (travelers, dates, budget)

2. **Data Exploration** (Cells 8-10):
   - Review weather forecasts for travel dates
   - Explore available activities in AgentsVille

3. **Initial Planning** (Cells 12-14):
   - Generate first itinerary using ItineraryAgent
   - Review initial travel plan

4. **Evaluation** (Cells 16-22):
   - Run comprehensive evaluation suite
   - Identify any issues with the plan

5. **Refinement** (Cells 32-37):
   - Use ItineraryRevisionAgent for improvements
   - Apply traveler feedback and fix issues

6. **Final Output** (Cells 38-40):
   - Display refined travel plan
   - Generate narrative trip summary

### Customization Options

#### Traveler Profiles
Modify `VACATION_INFO_DICT` to customize:
- Traveler names and ages
- Interest categories (art, cooking, comedy, technology, etc.)
- Travel dates
- Budget constraints

#### Model Selection
Choose from available OpenAI models:
- `GPT_41`: Strong general-purpose reasoning
- `GPT_41_MINI`: Balanced speed and performance (default)
- `GPT_41_NANO`: Fast and economical

#### Evaluation Criteria
The system includes multiple evaluation functions:
- **Date Validation**: Ensures dates match vacation parameters
- **Budget Compliance**: Verifies costs stay within budget
- **Interest Matching**: Confirms activities align with preferences
- **Weather Compatibility**: Prevents outdoor activities during bad weather
- **Activity Authenticity**: Validates against real activity database

## 🎮 Example Output

### Sample Vacation Configuration
```python
VACATION_INFO_DICT = {
    "travelers": [
        {
            "name": "Yuri",
            "age": 30,
            "interests": ["tennis", "cooking", "comedy", "technology"]
        },
        {
            "name": "Hiro", 
            "age": 25,
            "interests": ["reading", "music", "theatre", "art"]
        }
    ],
    "destination": "AgentsVille",
    "date_of_arrival": "2025-06-10",
    "date_of_departure": "2025-06-12", 
    "budget": 130
}
```

### Generated Itinerary Features
- **Day 1 (Clear Weather)**: Outdoor activities like tennis and sightseeing
- **Day 2 (Partly Cloudy)**: Mix of indoor and outdoor activities
- **Day 3 (Thunderstorm)**: Indoor alternatives like VR experiences and theaters

## 🔧 Technical Implementation

### AI Agent Architecture
- **System Prompts**: Carefully crafted prompts with role definitions, tasks, and constraints
- **Structured Output**: Pydantic models ensure consistent data formats
- **Tool Integration**: Function calling for external data and calculations
- **Error Handling**: Robust validation and fallback mechanisms

### ReAct Cycle Implementation
```
THOUGHT → ACTION → OBSERVATION → THOUGHT → ACTION → OBSERVATION → ...
```
- Iterative reasoning and action taking
- Tool-assisted problem solving
- Self-correction through evaluation feedback

### Weather Intelligence
- Real-time weather data integration
- LLM-based activity-weather compatibility assessment
- Automatic substitution of weather-inappropriate activities

## 📊 Evaluation Metrics

The system tracks multiple quality metrics:
- ✅ **Date Accuracy**: Start/end dates match vacation parameters
- ✅ **Budget Compliance**: Total cost ≤ specified budget
- ✅ **Activity Authenticity**: All activities exist in the database
- ✅ **Interest Satisfaction**: Each traveler has matching activities
- ✅ **Weather Safety**: No outdoor activities during storms
- ✅ **Feedback Integration**: Traveler preferences incorporated

## 🐛 Troubleshooting

### Common Issues

**Weather Compatibility Failures**
- Check if outdoor activities are scheduled during bad weather
- Run additional ReAct cycles to replace problematic activities
- Verify activity descriptions for weather suitability

**Budget Overruns**
- Use calculator tool to verify cost calculations
- Swap expensive activities for budget-friendly alternatives
- Check for duplicate cost calculations

**Missing Activities**
- Ensure activity IDs exist in the mock database
- Use exact activity data from API responses
- Avoid modifying activity details

## 🤝 Contributing

This project demonstrates advanced AI techniques for educational purposes. Key areas for enhancement:
- Additional evaluation criteria
- More sophisticated weather reasoning
- Extended activity categories
- Multi-city trip planning

## 📚 Learning Outcomes

By working through this project, you'll gain hands-on experience with:
- Advanced prompt engineering techniques
- Multi-agent AI system design
- Structured data validation with Pydantic
- ReAct reasoning pattern implementation
- LLM evaluation and feedback loops

## 📝 License

This project is part of the Udacity Agentic AI Nanodegree program and is intended for educational use.

---

**🎉 Congratulations!** You've successfully implemented a sophisticated AI travel planning system that showcases the power of modern LLM reasoning techniques!
