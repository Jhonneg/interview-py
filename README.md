# CrewAI Interview Preparation and Feedback

This project leverages CrewAI to simulate an interview process and provide detailed feedback on a candidate's response. It defines two main agents: an interviewer and a coach, who work together to generate interview questions and then evaluate the user's answer against the job description.

## Features

*   **Interview Question Generation**: An interviewer agent generates a relevant interview question based on a provided job description.
*   **Automated Feedback**: A coach agent evaluates the user's answer to the interview question, providing bullet-point feedback on what was good, what was lacking, and areas for improvement, specifically tailored to the job requirements (e.g., AWS, SaaS, architectural patterns).
*   **Customizable Roles**: Easily modify the interviewer's and coach's roles and goals to adapt to different interview scenarios.

## Setup

Follow these steps to set up and run the project:

1.  **Clone the repository:**

    ```bash
    git clone https://github.com/your-username/crewai-interview.git
    cd crewai-interview
    ```

2.  **Create a virtual environment:**

    ```bash
    python -m venv venv
    ```

3.  **Activate the virtual environment:**

    *   On macOS/Linux:
        ```bash
        source venv/bin/activate
        ```
    *   On Windows:
        ```bash
        .\venv\Scripts\activate
        ```

4.  **Install dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

5.  **Configure environment variables:**
    Create a  file in the project root directory with your OpenAI API key and any other necessary configurations.
    ```env
    OPENAI_API_KEY="your_openai_api_key_here"
    ```
    The project uses `dotenv` to load these variables.

## Usage

The project is designed to be run as a Jupyter notebook.

1.  **Open the notebook:**

    ```bash
    jupyter notebook main.ipynb
    ```

2.  **Run the cells:**
    Execute the cells in the  notebook sequentially. You will be prompted to enter the following information:
    *   Interviewer's name (e.g., "Matheus")
    *   Company name (e.g., "Eyna")
    *   Job position (e.g., "Desenvolvedor(a) Full Stack Júnior")
    *   Job description: Provide a detailed job description that the agents will use for context. This is crucial for generating relevant questions and feedback.

    The notebook will then:
    *   Initialize the `CrewAI` agents.
    *   Generate an interview question.
    *   Prompt you to provide your answer to the question.
    *   Provide feedback on your answer based on the job description.

Example of expected interaction:

```python
# filepath: /home/jonee/Work/crewai-interview/main.ipynb
# ...
interviewer = input("Enter the name of the interviewer: ")
company = input("Enter the name of the company: ")
job_position = input("Enter the job position: ")
job_description = input("Enter the job description: ")
```

# Demo 

**Interview agent initializing**
<img width="976" height="477" alt="screenshot-2025-12-14_23-11-06" src="https://github.com/user-attachments/assets/c111344c-1ca1-4e44-a342-90bce2b4b2b2" />
**Interview agent question**
<img width="1757" height="232" alt="screenshot-2025-12-14_23-11-27" src="https://github.com/user-attachments/assets/d4437fb2-9a9d-494b-bbf1-4896a4477fc7" />
**Coach Agent Feedback**
<img width="950" height="830" alt="screenshot-2025-12-14_23-10-31" src="https://github.com/user-attachments/assets/a762f9bf-d70e-4023-91fa-3edcfca24e3d" />




