# LLM for Music Recommendation Using Facial Expressions

## Overview
This project creates an innovative music recommendation system that analyzes facial expressions in real-time to detect emotions and suggest appropriate music. By leveraging computer vision and machine learning technologies, the system provides personalized music experiences based on the user's current emotional state.

## Key Features
- **Real-time Facial Expression Detection**: Captures and analyzes facial expressions continuously using webcam feed
- **Emotion Classification**: Identifies 7 basic emotions (happy, sad, angry, surprised, fearful, disgusted, neutral)
- **Dynamic Music Recommendation**: Suggests music genres and playlists based on detected emotions
- **Adaptive Learning**: Improves recommendations based on user feedback
- **Intuitive User Interface**: Clean, responsive interface built with Streamlit

## Technical Architecture

### Emotion Detection Pipeline
1. **Face Detection**: Using OpenCV's Haar cascades or DNN models
2. **Facial Landmark Detection**: Identifies key facial points
3. **Emotion Classification**: Pre-trained CNN models analyze facial features
4. **Emotion-Music Mapping**: Maps detected emotions to appropriate music categories

### Technologies Used
- **Python**: Core programming language
- **OpenCV**: Computer vision library for facial detection and processing
- **TensorFlow/Keras**: For CNN model implementation
- **Streamlit**: For interactive web application interface
- **NLP**: For processing music metadata and creating appropriate mappings
- **Machine Learning**: CNN models for emotion classification
- **Visual Studio**: IDE for development

## Setup Instructions

### Prerequisites
- Python 3.8+
- Webcam
- Internet connection for music API access

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/name/repo.git
   cd facial-music-recommendation
   ```

2. Create and activate virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Download pre-trained models:
   ```bash
   python download_models.py
   ```

5. Run the application:
   ```bash
   streamlit run app.py
   ```

6. Access the web interface at `http://localhost:8501`

## Emotion-Music Mapping

The system maps detected emotions to music genres as follows:

| Emotion | Music Genres/Characteristics |
|---------|------------------------------|
| Happy | Pop, Dance, Upbeat songs |
| Sad | Soft Rock, Ballads, Melancholic songs |
| Angry | Heavy Metal, Intense Rock, High-energy tracks |
| Surprised | Experimental, Jazz, Unpredictable compositions |
| Fearful | Ambient, Calming, Reassuring tracks |
| Disgusted | Punk, Alternative, Unconventional music |
| Neutral | Classical, Instrumental, Moderate tempo |

## System Architecture
```
User Webcam → OpenCV Face Detection → Facial Landmark Extraction → 
CNN Emotion Classification → Emotion-Music Mapping → 
Music API Integration → Music Recommendation → User Interface
```

## Performance Metrics
- Emotion detection accuracy: ~87% on benchmark datasets
- Average processing time: <100ms per frame
- Recommendation relevance: Determined through user feedback

## Future Enhancements
- Multi-face emotion detection
- Integration with popular music streaming platforms (Spotify, Apple Music)
- Expanded emotion detection (beyond 7 basic emotions)
- Personalized learning based on individual preferences
- Mobile application development

## Troubleshooting
- **Camera Access Issues**: Ensure browser permissions are granted for camera access
- **Slow Performance**: Adjust frame processing rate in settings
- **Emotion Misdetection**: Improve lighting conditions for better detection

## Contributors
- [Your Name]
- [Team Member Names]

## License
MIT License
