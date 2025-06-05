# EduAI


A Python-based application that analyzes student test data, generates insightful visualizations, and produces AI-powered feedback reports—all wrapped in a professional PDF export.

## Features

- Visual dashboard with subject/chapter-wise metrics  
- AI-generated personalized feedback using LLMs  
- PDF report generation with embedded charts and styled sections  
- Web interface via Gradio  
- Easy JSON-based data upload

---

## APIs Used

### 1. **OpenRouter API (DeepSeek LLM)**
- Used for generating personalized feedback through a prompt-based interaction.
- Model used: `deepseek-coder`, hosted via OpenRouter.
- Endpoint accessed through HTTPS with proper authorization headers.
- Enables structured, human-like educational mentorship response based on student data.

### 2. **Gradio**
- Used to create the interactive web interface (`gr.Blocks()`).
- Components: File upload, Analyze button, Markdown/text/image outputs, downloadable PDF.

### 3. **Google Colab**
- Environment used for development, testing, and demo deployment.
- Allows integration of Python code with Gradio UI, matplotlib, pandas, and FPDF libraries.

---

## Prompt Logic for AI Feedback

A structured prompt is dynamically generated using actual student performance data. Here's a breakdown of the logic:

```text
You are an experienced educational mentor providing personalized feedback...

STUDENT'S TEST PERFORMANCE SUMMARY:
- Total Time Taken: <formatted_time>
- Total Marks Scored: <marks>
- Questions Attempted: <attempts>
- Overall Accuracy: <accuracy>%

Please provide a comprehensive, personalized feedback report with:
1. MOTIVATIONAL OPENING
2. DETAILED PERFORMANCE ANALYSIS
3. KEY INSIGHTS & OBSERVATIONS
4. ACTIONABLE IMPROVEMENT STRATEGIES
5. PERSONALIZED STUDY PLAN
6. ENCOURAGING CONCLUSION

