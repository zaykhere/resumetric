# ResuMetric

ResuMetric is a powerful, AI-driven resume analyzer designed to help job seekers optimize their resumes for Applicant Tracking Systems (ATS) and specific job descriptions. Built with a modern tech stack and powered by **Puter.js**, it offers detailed feedback, scoring, and actionable improvements.

![Analyzed Resume](https://res.cloudinary.com/zainhither/image/upload/v1770726290/your_folder_name/Untitled2_cqpydv.png)

## 🚀 Features

-   **AI-Powered Analysis**: Utilizes Claude 3.5 Sonnet (via Puter.js AI) to analyze resumes against job descriptions.
-   **ATS Scoring**: Provides a compatibility score to estimate how well a resume passes automated screening.
-   **Detailed Feedback**: Offers specific, actionable advice on content, formatting, and keywords.
-   **PDF to Image Conversion**: Automatically converts uploaded PDFs to high-quality images for visual reference alongside feedback.
-   **Secure Cloud Storage**: Leveraging Puter.js File System and Key-Value Store to save resumes and analysis history securely.
-   **Authentication**: Integrated sign-in system using Puter.js Auth.

## 🛠️ Tech Stack

-   **Frontend Framework**: [React 19](https://react.dev/) (via [React Router 7](https://reactrouter.com/))
-   **Build Tool**: [Vite](https://vitejs.dev/)
-   **Styling**: [Tailwind CSS v4](https://tailwindcss.com/)
-   **Backend & Cloud Services**: [Puter.js](https://docs.puter.com/) (Auth, AI, File System, KV Store)
-   **State Management**: [Zustand](https://zustand-demo.pmnd.rs/) with `puter.ts` store
-   **PDF Processing**: [pdfjs-dist](https://mozilla.github.io/pdf.js/)

## 📦 Prerequisites

Before you begin, ensure you have the following installed:
-   [Node.js](https://nodejs.org/) (v20 or higher recommended)
-   npm (usually comes with Node.js)

## 🏁 Getting Started

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/zaykhere/resumetric.git
    cd resumetric
    ```

2.  **Install dependencies:**
    ```bash
    npm install
    ```

3.  **Run the development server:**
    ```bash
    npm run dev
    ```

4.  **Open your browser:**
    Navigate to `http://localhost:5173` to view the application.

## 🔧 How It Works

Resumetric leverages **Puter.js** as a comprehensive backend-as-a-service:

1.  **Auth**: Users sign in with their Puter.js account, ensuring their data is private and persistent.
2.  **Storage**:
    -   **File System (`fs`)**: Uploaded resumes (PDFs) and their converted images are stored directly in the user's Puter.js cloud directory.
    -   **KV Store (`kv`)**: Metadata (Company Name, Job Title, Analysis results) is stored in the Puter.js Key-Value key-value store (`resume:*`) for quick retrieval.
3.  **AI Analysis (`ai` chat)**:
    -   The app sends the resume text (extracted via privacy-preserving and efficient methods) and the job description to the AI model.
    -   The AI evaluates the match, generating a score and structured feedback using a prompt specifically tuned for resume analysis.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1.  Fork the project
2.  Create your feature branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

Built with ❤️ using [React Router](https://reactrouter.com/) and [Puter.js](https://puter.com).
