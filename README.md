Overview
Eat in Sight is an intelligent Telegram bot that uses AI-powered image recognition to analyze food photos and provide detailed nutritional breakdowns. Users can simply send a picture of their meal to receive instant nutritional analysis and have their data automatically logged in a Notion database for tracking.

Key Features
Smart Meal Recognition
Image Processing: Analyzes food photos using Google Gemini AI

Food Identification: Automatically detects multiple food items in a single image

Portion Estimation: Calculates approximate portion sizes for accurate nutrition tracking

Comprehensive Nutritional Analysis
Macronutrient Breakdown: Detailed protein, carbs, and fat analysis

Calorie Calculation: Total and per-item calorie counts

Confidence Scoring: Indicates analysis accuracy level (high/low confidence)

Telegram Integration
Real-time Interaction: Instant responses via Telegram messaging

User-friendly Interface: Simple photo-based interaction

Personalized Responses: Addresses users by name with formatted messages

Automatic Data Logging
Notion Integration: Automatically saves all meal data to a structured database

Historical Tracking: Maintains complete meal history with timestamps

Nutrition Dashboard: Enables long-term dietary pattern analysis

Technical Architecture
Message Processing Pipeline
Telegram Input Handling
Trigger: Listens for incoming Telegram messages (text or photos)

User Identification: Captures user ID and name for personalized responses

Content Detection: Differentiates between commands and photo uploads

Smart Routing System
Switch Node: Routes messages based on content type:

Command Path: Handles text commands (future expansion)

Photo Path: Processes food images for analysis

Image Processing Chain
File Retrieval: Downloads the highest quality version of the uploaded photo

Base64 Conversion: Prepares image for AI analysis

AI Vision Analysis: Uses Google Gemini to identify food and calculate nutrition

AI Analysis Engine
Google Gemini Integration
Model: gemini-2.5-pro for advanced image recognition

Structured Output: Enforces JSON-only responses for consistent data parsing

Nutrition Expertise: Specialized prompt for food identification and portion estimation

Analysis Components
Food Item Detection: Identifies individual components of the meal

Portion Size Estimation: Calculates approximate quantities

Nutrition Calculation: Provides macronutrient breakdown per item

Confidence Assessment: Evaluates analysis accuracy

Data Processing & Output
Response Formatting
JSON Parsing: Extracts structured data from AI response

Message Creation: Formats user-friendly Telegram response

Error Handling: Graceful fallback for parsing failures

Dual Output System
User Notification: Sends formatted nutrition report back to user

Data Persistence: Automatically logs meal data to Notion database

Data Flow
Input Processing
Telegram Message → Extract User Data → Detect Content Type → Route to Photo Analysis

Photo Analysis Pipeline
Get Photo File → Convert to Base64 → AI Image Analysis → Parse JSON Response

Output Generation
Format User Message + Prepare Notion Data → Send Telegram Response + Log to Database

Nutritional Analysis Output
Structured Data Format
The AI returns detailed nutritional information including:

Meal description and food items identified

Individual portion sizes and nutrition per item

Total calories and macronutrient summary

Confidence level in the analysis

User Report Format
The bot sends formatted messages including:

Meal description and food items list

Individual nutrition breakdown per food item

Total nutrition summary with calories and macros

Confidence indicator for accuracy assessment

Notion Database Integration
Data Structure
Meal Name: AI-generated description of the meal

Date: Automatic timestamp of analysis

Food Items: Concatenated list with portions and nutrition

Macronutrients: Separate fields for protein, carbs, fat

Total Calories: Sum of all food items

Automated Logging
Real-time Sync: Immediate database entry after analysis

Structured Format: Consistent data organization for reporting

Historical Record: Complete meal history for trend analysis

Use Cases & Benefits
For Health-Conscious Users
Quick Nutrition Tracking: Photo-based logging代替manual entry

Portion Awareness: AI estimation helps understand serving sizes

Diet Monitoring: Track macronutrient balance over time

Meal Planning: Historical data informs future food choices

For Fitness Enthusiasts
Protein Tracking: Monitor daily protein intake

Calorie Management: Maintain energy balance

Macro Optimization: Adjust ratios for specific fitness goals

For Medical Conditions
Dietary Compliance: Track specific nutritional requirements

Portion Control: Maintain consistent serving sizes

Nutritional Awareness: Understand food composition better

Setup & Configuration
Prerequisites
Telegram Bot Token: For messaging interface

Google Gemini API: For image analysis and nutrition calculation

Notion Integration: For data storage and tracking

n8n Workflow Platform: For automation orchestration

Customization Options
Nutrition Databases: Connect to different tracking systems

Report Formatting: Adjust message templates and detail level

Additional Analysis: Expand to include micronutrients or allergens

Integration Options: Connect with fitness apps or health platforms

Quality Assurance Features
Confidence Scoring: Transparent accuracy indicators

Error Handling: Graceful failure recovery

Data Validation: Ensures nutritional calculations are reasonable

Consistent Formatting: Standardized output for reliable user experience

This system provides a seamless, AI-powered nutrition tracking experience that eliminates manual data entry while delivering accurate, actionable nutritional insights through a simple photo-based interface.
