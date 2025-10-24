 project demonstrates a simple yet powerful AI Agent workflow built using n8n and OpenAI. The AI Agent can process inputs, make API calls, and generate intelligent responses based on user data or triggers.

🚀 Features

Integration with OpenAI GPT models

Automated workflows using n8n

Custom input handling and response generation

Looping and rate limit management using SplitInBatches and Wait nodes

Error handling for Insufficient Quota, Bad Request, and Rate Limit

⚙️ Setup Instructions
1. Clone the Repository
git clone https://github.com/your-username/ai-agent.git
cd ai-agent

2. Install Dependencies

Ensure you have n8n installed globally:

npm install -g n8n


Or run it using Docker:

docker run -it --rm \
  -p 5678:5678 \
  -v ~/.n8n:/home/node/.n8n \
  n8nio/n8n

3. Configure Environment Variables

Create a .env file with your OpenAI API key:

OPENAI_API_KEY=your_api_key_here

🧠 How It Works

The workflow consists of the following main components:

Manual Trigger Node – starts the workflow manually

SplitInBatches Node – processes data in manageable chunks

OpenAI Node – connects to GPT model for text generation

Wait Node – prevents rate-limit errors by delaying requests

You can import the sample workflow JSON (ai-agent-workflow.json) into n8n to get started instantly.

🧩 Troubleshooting
Common Issues:

Rate Limit Error: Add a Wait node between requests.

Insufficient Quota: Check your OpenAI account balance and ensure the correct API key.

Bad Request: Validate all input parameters.

📁 Folder Structure
ai-agent/
│
├── images/               # Workflow and concept images
├── workflow/             # n8n workflow JSON files
├── README.md             # Project documentation
└── .env                  # Environment configuration

📸 Screenshot

<img width="1920" height="1080" alt="2025-10-24 (11)" src="https://github.com/user-attachments/assets/9ffcb892-9467-4270-ad1f-b106a5aebc80" />

🧑‍💻 Author

Pooja Paithanpagare
💡 Aspiring Java Full Stack Developer passionate about AI automation and workflow integration.
