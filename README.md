# LeetCode Problem Solver

## Description

This Python script automates the process of solving LeetCode problems using web automation and the Claude AI API. It navigates through LeetCode's problem set, selects problems, generates solutions using Claude AI, and submits them automatically.

## Features

- Automated login to LeetCode
- Navigation through LeetCode's problem set
- Problem selection based on availability and difficulty
- Code generation using Claude AI
- Automated code submission and error handling
- Retries with improved solutions on failures

## Requirements

- Python 3.x
- Selenium WebDriver
- undetected_chromedriver
- anthropic Python library
- BeautifulSoup4

## Setup

1. Install required Python packages:
   ```
   pip install selenium undetected_chromedriver anthropic beautifulsoup4
   ```

2. Set up your LeetCode credentials:
   - Update `LEETCODE_USERNAME` and `LEETCODE_PASSWORD` in the script with your LeetCode credentials.

3. Set up Claude API:
   - Obtain an API key from Anthropic
   - Replace `API_KEY` in the script with your actual API key

## Usage

Run the script using Python:

1. CD to wherever you have the file stored.
2. Execute the script:
   ```
   python Solver.py
   ```

The script will automatically:
- Log in to LeetCode
- Navigate through problems
- Select a problem
- Generate a solution using Claude's 3.5 Sonnet API AI
- Submit the solution
- Handle any errors and retry if necessary
- Move on to the next problem

## Configuration

You can modify the following constants in the script to adjust its behavior:

- `MAX_RETRIES`: Maximum number of attempts for each problem (1 = no retries, 2 = 1 retry, etc.)
- `LEETCODE_PROBLEMSET_URL`: Starting URL for problem navigation.
- `CLAUDE_MODEL`: The Claude AI model to use.
- `MAX_TOKENS`: Maximum tokens for Claude API responses.
- `TEMPERATURE`: Temperature setting for Claude API.

## Notes

This project demonstrates the viability of 'real-language programming'. It was built using natural language instructions submitted to an AI, creating a code-based tool that writes code solutions.

Building a system that can solve a massive amount of problems much faster than a normal person is valuable. The ability to create such a system without writing code from memory, but rather by describing the desired functionality, showcases a new paradigm in software development.

While the code produced by this system may not be the most reliable, readable, fastest, memory-efficient, or scalable, it represents a stepping stone towards more advanced AI-assisted programming. As AI systems improve, so will the quality of the generated code.

There are many instances where the power of AI systems to solve problems can be more valuable than traditional hard-coding approaches. At the very least, partner programming with an AI is becoming an increasingly viable and powerful option.

The "Sleep(5)" statements are horrendous, I know that, but Leetcode has some hidden rate limits it throws on suspicious accounts, this fixes that.

## Disclaimer

This script is for educational purposes only. Use responsibly and in accordance with LeetCode's terms of service.
