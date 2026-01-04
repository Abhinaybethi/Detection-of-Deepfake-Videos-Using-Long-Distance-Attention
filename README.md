# Detection of Deepfake Videos Using Long Distance Attention

A Django-based web application for detecting deepfake videos using long-distance attention mechanisms. This project implements advanced machine learning techniques to identify manipulated videos and distinguish them from authentic content.

## 📋 Overview

This application leverages spatial and temporal artifacts analysis with attention mechanisms to detect deepfake videos. It provides a user-friendly web interface for uploading videos and receiving predictions about their authenticity.

## 🌟 Features

- **Video Upload & Analysis**: Upload videos for deepfake detection
- **User Authentication**: Secure login and registration system
- **Admin Dashboard**: Service provider interface for monitoring predictions
- **Data Visualization**: Charts and graphs showing prediction statistics
- **Model Training**: Interface for training the detection model
- **Export Results**: Download prediction datasets in Excel format
- **Profile Management**: User profile viewing and management

## 🛠️ Technology Stack

- **Backend**: Django 3.0.5
- **Database**: SQLite3 (configurable to MySQL)
- **Machine Learning**: TensorFlow 2.1.0, Keras 2.3.1
- **Data Processing**: Pandas, NumPy, Scikit-learn
- **Computer Vision**: OpenCV
- **Visualization**: Matplotlib

## 📦 Installation

### Prerequisites

- Python 3.7 or higher
- pip (Python package manager)
- Git

### Setup Instructions

1. **Clone the repository**
   ```bash
   git clone https://github.com/Abhinaybethi/Detection-of-Deepfake-Videos-Using-Long-Distance-Attention.git
   cd Detection-of-Deepfake-Videos-Using-Long-Distance-Attention
   cd Detection_of_Deepfake_Videos/Detection_of_Deepfake_Videos
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv_new
   ```

3. **Activate the virtual environment**
   - On Windows:
     ```bash
     venv_new\Scripts\activate
     ```
   - On macOS/Linux:
     ```bash
     source venv_new/bin/activate
     ```

4. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

5. **Run database migrations**
   ```bash
   cd detection_of_deepfake_videos
   python manage.py migrate
   ```

6. **Create a superuser (optional)**
   ```bash
   python manage.py createsuperuser
   ```

7. **Run the development server**
   ```bash
   python manage.py runserver
   ```

8. **Access the application**
   - Open your browser and navigate to: `http://127.0.0.1:8000/`

## 🗂️ Project Structure

```
Detection_of_Deepfake_Videos/
├── detection_of_deepfake_videos/
│   ├── Remote_User/              # User-facing application
│   ├── Service_Provider/         # Admin/service provider interface
│   ├── Template/                 # HTML templates and static files
│   │   ├── htmls/               # HTML templates
│   │   ├── images/              # Static images
│   │   └── media/               # Uploaded media files
│   ├── detection_of_deepfake_videos/  # Django project settings
│   │   ├── settings.py          # Configuration settings
│   │   ├── urls.py              # URL routing
│   │   └── wsgi.py              # WSGI configuration
│   ├── manage.py                # Django management script
│   ├── Datasets.csv             # Training datasets
│   └── Results.csv              # Prediction results
├── Database/                     # Database files
│   └── detection_of_deepfake_videos.sql
├── requirements.txt              # Python dependencies
└── README.md                     # This file
```

## 🚀 Usage

### For End Users (Remote Users)

1. **Register**: Create a new account at `/Register1/`
2. **Login**: Access your account at `/login/`
3. **Upload Video**: Navigate to "Predict Video Type" to upload and analyze videos
4. **View Profile**: Check your profile and prediction history
5. **View Results**: See the prediction results for your uploaded videos

### For Service Providers (Admins)

1. **Login**: Access admin panel at `/serviceproviderlogin/`
2. **View Users**: Monitor registered users
3. **Train Model**: Train the deepfake detection model
4. **View Analytics**: Access charts and statistics
5. **Download Data**: Export prediction datasets

## 📊 Available Endpoints

- `/` - Home page
- `/login/` - User login
- `/Register1/` - User registration
- `/Predict_Video_Type/` - Video upload and prediction
- `/ViewYourProfile/` - User profile
- `/serviceproviderlogin/` - Admin login
- `/View_Remote_Users/` - View all users (admin)
- `/train_model/` - Train detection model (admin)
- `/View_Prediction_Of_Video_Type/` - View all predictions (admin)
- `/Download_Predicted_DataSets/` - Export results (admin)

## 🔧 Configuration

### Database Configuration

The project is configured to use SQLite by default. To use MySQL:

1. Install MySQL server
2. Create a database named `detection_of_deepfake_videos`
3. Update `settings.py`:
   ```python
   DATABASES = {
       'default': {
           'ENGINE': 'django.db.backends.mysql',
           'NAME': 'detection_of_deepfake_videos',
           'USER': 'your_mysql_user',
           'PASSWORD': 'your_mysql_password',
           'HOST': '127.0.0.1',
           'PORT': '3306',
       }
   }
   ```
4. Install MySQL client: `pip install mysqlclient`

## 📝 Dependencies

See `requirements.txt` for a complete list of dependencies:

- Django==3.0.5
- numpy==1.18.2
- pandas==1.0.3
- Pillow==7.1.1
- scikit-learn==0.22.2
- tensorflow==2.1.0
- keras==2.3.1
- opencv-python==4.2.0.34
- matplotlib==3.2.1
- xlwt (for Excel export)

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is part of academic research based on the IEEE Transactions on Neural Networks and Learning Systems publication (Issue Date: 06 January 2023).

## 🔬 Research Background

This implementation is based on research in:
- Deepfake detection
- Face manipulation detection
- Attention mechanisms
- Spatial and temporal artifact analysis

## 📧 Contact

For questions or support, please open an issue in the GitHub repository.

## 🙏 Acknowledgments

- IEEE Transactions on Neural Networks and Learning Systems
- Django Framework
- TensorFlow and Keras communities
- OpenCV contributors

## ⚠️ Disclaimer

This tool is for educational and research purposes. Always verify results and use responsibly.

---

**Note**: The application is currently running on Django's development server. For production deployment, please configure a production-ready server (e.g., Gunicorn, uWSGI) and use a production database.
