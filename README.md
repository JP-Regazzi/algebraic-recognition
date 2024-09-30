# Algebraic Recognition System

## Overview

This project is an **Algebraic Recognition Engine** designed to automatically assess the accuracy of students' algebraic answers. By comparing mathematical expressions provided by students with correct answers, the system quantifies their similarity and offers detailed feedback on errors. The platform is developed to be faster, more consistent, and objective compared to traditional human-based correction methods.

The engine leverages techniques such as **tree edit distance** to compare algebraic expressions, providing real-time feedback to users, and helps students identify mistakes in their equations, such as sign errors, wrong variables, or incorrect unary operations.

### Core Features

- **Automatic assessment of algebraic expressions**
- **Detailed feedback generation** (quantitative and qualitative)
- **Semantic and syntactic comparison of expressions**
- **Integration with React-based frontend for a user-friendly interface**
- **Utilizes machine learning techniques like Graph Convolutional Networks and Graph Attention Networks to enhance expression comparison**

## Project Structure

### Backend

The backend is built with **FastAPI** and handles the processing of algebraic expressions. Key functionalities include:

- **SymPy Integration**: Converts and simplifies expressions for comparison.
- **Tree Edit Distance**: Quantifies the similarity between expression trees.
- **Feedback System**: Detects errors such as wrong signs, incorrect variables, and missing terms.
- **Machine Learning Integration**: Uses pre-trained models (such as **BERT** and custom neural networks) for advanced expression comparison.

### Frontend

The frontend is developed using **React**, enabling a smooth and interactive user experience. Users input their expressions in LaTeX format, and the system instantly processes and provides feedback.

### Key Python Files:

- **`main.py`**: 
  - Handles API requests from the frontend.
  - Routes for comparing expressions (`/get_score`) and providing feedback (`/get_feedback`).
- **`engine.py`**: 
  - Core logic for comparing expressions using SymPy and tree structures.
  - Functions for simplifying expressions, calculating tree edit distance, and detecting specific types of algebraic errors.

### Core Algorithms

- **Tree Edit Distance**: Measures the minimal number of operations (insertions, deletions, substitutions) required to transform one expression into another.
- **Graph Neural Networks**: Utilized for learning embeddings of mathematical expressions, which are then compared to quantify their similarity.
- **Feedback Mechanisms**: Detect specific types of errors such as:
  - **Sign errors**: Incorrect signs in the expression.
  - **Variable mismatch**: Wrong variables used.
  - **Unary operation errors**: Incorrect application of unary operators.

## How to Run

### Prerequisites

Ensure you have the following installed:

- **Python 3.8+**
- **Node.js** (for the frontend)
- **npm** (for React)

### Backend Setup

1. Clone the repository:
    ```bash
    git clone https://github.com/your-repo/algebraic-recognition-system.git
    cd algebraic-recognition-system
    ```

2. Install backend dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Run the FastAPI server:
    ```bash
    uvicorn main:app --reload
    ```

### Frontend Setup

1. Navigate to the `frontend` directory:
    ```bash
    cd frontend
    ```

2. Install frontend dependencies:
    ```bash
    npm install
    ```

3. Run the React development server:
    ```bash
    npm start
    ```

### Usage

Once both servers are running, navigate to `http://localhost:3000` to use the system. Input your algebraic expressions in LaTeX format and receive instant feedback on the correctness of your answer.

## Authors

- **Abderrahmane Dkour**
- **Lucas Fernandes Martins**
- **João Pedro Regazzi Ferreira Da Silva**
- **Gabriel Souza Lima**
- **Salma Maazoum**

---
