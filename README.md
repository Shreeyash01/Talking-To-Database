
# 🗃️ Talking To Database!

<p align="center">
  <img src="https://github.com/Shreeyash01/temp/assets/103109932/403b0f4c-a3b2-464e-be72-7a4064e79f78" alt="Talking-To-Database Banner">
</p>

**Talking-To-Database** is a full-stack web application that allows users to interact with a MySQL database using natural language inputs. The application uses a fine-tuned TinyLlama model to convert natural language queries into SQL statements, making database interactions more intuitive and user-friendly.

## ✨ Features

- 🎤 **Text and Voice Input:** Accepts user input via text or voice using the React Speech Recognition library.
- 🔍 **SQL Query Generation:** Converts natural language inputs into SQL queries using a fine-tuned TinyLlama model.
- ✏️ **Query Confirmation:** Allows users to edit or confirm the generated SQL query before execution.
- 💾 **Database Interaction:** Executes the confirmed SQL query on a MySQL database and returns the results to the frontend.

## 🛠️ Technologies Used

- **Frontend:** React.js, Bootstrap, Tailwind CSS
- **Backend:** Python Flask
- **Database:** MySQL
- **Machine Learning:** TinyLlama model fine-tuned on a custom SQL dataset

## 📁 Project Structure

```
├── client                   # React.js frontend
│   ├── public
│   ├── src
│   └── package.json
├── server                   # Python Flask backend
│   ├── main.py
│   ├── model                # Directory which Contains the fine tuned model (not uploaded to GitHub)
├── .gitignore
└── README.md
```

## 🚀 Setup Instructions

### Prerequisites

- Node.js and npm
- Python 3.x
- MySQL server

### Frontend Setup

1. Navigate to the `client` directory:
   ```sh
   cd client
   ```

2. Install dependencies:
   ```sh
   npm install
   ```

3. Start the React development server:
   ```sh
   npm start
   ```

### Backend Setup

1. Navigate to the `server` directory:
   ```sh
   cd server
   ```

2. Create a virtual environment and activate it:
   ```sh
   python -m venv venv
   source venv/bin/activate   # On Windows use `venv\Scripts\activate`
   ```
3. Download the **[Fine-Tuned Model](https://drive.google.com/drive/u/1/folders/1CHI1xFjE35ePHWB_0dp_Ak1rrS9D1kvo)** and update the model path in  `main.py`.

4. Configure the MySQL database in `main.py`.

5. Start the Flask server:
   ```sh
   python main.py
   ```

### Database Setup

1. Create a MySQL database and update the database configuration in `main.py`.
2. Populate the database with your schema and data.

## 📊 Fine-Tuned Model and Dataset

- **[Dataset](https://huggingface.co/datasets/shreeyashm/SQL-Queries-Dataset) :** The custom dataset used to fine-tune the TinyLlama model can be found here.
- **[Pre Trained Model](https://huggingface.co/TheBloke/TinyLlama-1.1B-Chat-v1.0-GGUF) :** The pre-trained TinyLlama model can be accessed here.

## 🧠 Model Fine-Tuning Process

The TinyLlama model was fine-tuned on a custom SQL dataset using the following steps:

1. **Dataset Preparation:** Created a dataset with columns for natural language questions, SQL context, and SQL queries.
2. **Quantization:** Converted the model to a 4-bit quantized format using the `bitsandbytes` library.
3. **Training:** Used the `SFTTrainer` with QLoRA (Quantized Low Rank Adaption) technique for efficient fine-tuning.
4. **Model Integration:** Combined the fine-tuned parameters with the TinyLlama model for inference.

## 💻 Usage

Screenshots -
![Usage Gif](https://github.com/Shreeyash01/temp/assets/103109932/357b9508-360c-4f1f-a95c-68da94df01f1)
![Usage Gif](https://github.com/Shreeyash01/temp/assets/103109932/ae8c20ed-ae96-4f32-984a-b6a0bec8e1b4)

1. Input your query in natural language via text or voice.
2. Review and confirm the generated SQL query.
3. Execute the query to interact with the MySQL database and view the results.

## 🤝 Contributing

Contributions are welcome! Please open an issue or submit a pull request for any improvements or bug fixes.

## 📜 License

This project is licensed under the MIT License.

## 🙏 Acknowledgements

- [Hugging Face](https://huggingface.co) for the TinyLlama model.
- [Google Colab](https://colab.research.google.com) for providing the free GPU resources for model fine-tuning.

---
