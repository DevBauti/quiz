# FQuiz Documentation

## Overview

QuizTools generates educational quizzes in Spanish from uploaded files (PDF, text, CSV) using an AI agent.

## Features

- Processes files via webhook input.
- Extracts content from PDF, text, CSV.
- Generates quizzes with OpenAI Chat Model.
- Outputs structured JSON responses.

## Installation

1. Clone the repository.
2. Install dependencies: `npm install`.
3. Configure OpenAI API credentials.

## Usage

1. Upload a file (e.g., `el-fantasma-de-canterville-oscar-wilde.pdf`) via webhook.
2. Workflow extracts text, creates quiz questions.
3. Receive JSON output with questions and answers.

## Workflow Diagram

![Workflow Diagram](images\FQuizWF.jpg)

## Screenshots

- **Main Interface**:  
  ![Main Interface](images\WindowsFQuiz.jpeg)

## Configuration

- Edit `Webhook` node for custom path.
- Update `OpenAI Chat Model` with API credentials.
- Adjust `AI Agent` prompt for specific rules.

## License

MIT License