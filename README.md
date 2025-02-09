# Virtual_health_assistant

# Medical Image Analytics

## Overview

**Medical Image Analytics** is an application that leverages AI to analyze uploaded medical images and provide detailed insights regarding potential health issues. The tool uses a specialized generative AI model to examine medical images, offering analysis in the form of detailed findings, recommendations, and treatment suggestions. It also ensures safety by applying multiple content filters to maintain high ethical standards.

## Features

- **Image Upload**: Upload medical images in PNG, JPEG, or JPG format.
- **Automated Analysis**: Generate detailed reports based on the uploaded medical images, identifying potential health issues.
- **Structured Reporting**: The analysis includes four key sections:
  1. **Detailed Analysis**: In-depth examination of the image, highlighting anomalies.
  2. **Finding Report**: Clear documentation of any observed abnormalities or diseases.
  3. **Recommendations and Next Steps**: Suggested further actions or tests to take based on the findings.
  4. **Treatment Suggestions**: Recommended treatment or interventions if applicable.
- **Safety Settings**: The app ensures that harmful content such as harassment, hate speech, explicit content, and dangerous material is blocked through a strict filtering system.

## Installation

### Prerequisites

- Python 3.8 or higher
- Streamlit library
- Google Generative AI API Key

### Steps to Install

1. Clone this repository to your local machine:
    ```bash
    git clone https://github.com/your-username/medical-image-analytics.git
    cd medical-image-analytics
    ```

2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Obtain a Google Generative AI API Key by setting up access to Google's generative AI platform, and store it in a file named `api_key.py` as:
    ```python
    api_key = "your_google_api_key"
    ```

4. Run the Streamlit app:
    ```bash
    streamlit run app.py
    ```

## Usage

- Open the app in your browser.
- Upload a medical image (PNG, JPEG, or JPG) using the file upload feature.
- Click "Generate the Analysis" to get the AI-generated report.
- The application will display the analysis report based on the uploaded image.

## Configuration

The system is configured to:
- Use the **Gemini-1.5-Flash** model for content generation.
- Set specific **safety settings** to block harmful content.
- Apply a **structured approach** to the analysis, with clearly defined sections such as findings, recommendations, and treatment options.

### Model Settings

The following model configuration is used:
```python
generation_config = {
    "temperature": 0.4,
    "top_p": 1,
    "top_k": 32,
    "max_output_tokens": 4896,
}
