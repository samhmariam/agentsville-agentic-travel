# AgentsVille Trip Planner 🏙️✈️

An advanced AI-powered travel planning system that demonstrates cutting-edge LLM reasoning techniques including role-based prompting, chain-of-thought reasoning, ReAct prompting, and feedback loops.

## 🎯 Project Overview

This project implements an intelligent travel agent that plans the perfect vacation to the wonderful city of AgentsVille! The system uses multiple AI agents and reasoning patterns to create personalized, weather-aware itineraries that satisfy traveler preferences and constraints.

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

