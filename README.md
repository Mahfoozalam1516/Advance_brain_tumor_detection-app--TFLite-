# Brain Tumor Detection App (TFLite)

An advanced web application for brain tumor detection using TensorFlow Lite and Streamlit. This application provides a user-friendly interface for analyzing MRI scans and detecting different types of brain tumors.

## Features

- **Single Image Analysis**: Upload and analyze individual MRI scans
- **Batch Processing**: Process multiple images simultaneously
- **Image Enhancement**: Automatic image enhancement for better analysis
- **Detailed Reporting**: Generate comprehensive PDF reports
- **Analytics Dashboard**: Track and visualize analysis history
- **Image Comparison**: Compare multiple MRI scans side by side
- **Email Notifications**: Optional email alerts for analysis results
- **Dark/Light Mode**: Adjustable UI theme
- **Export Options**: Download results in CSV or Excel format

## Installation

1. Clone the repository:

```bash
git clone https://github.com/yourusername/brain-tumor-detection.git
cd brain-tumor-detection
```

2. Create a virtual environment (recommended):

```bash
python -m venv venv
source venv/bin/activate  # On Windows, use: venv\Scripts\activate
```

3. Install required packages:

```bash
pip install -r requirements.txt
```

## Model Setup

1. Ensure you have the TFLite model file `brain_tumor_model_quantized.tflite` in the project root directory
2. The model should accept 150x150 RGB images as input
3. The model should output predictions for four classes: Glioma, Meningioma, No Tumor, and Pituitary

## Usage

1. Start the Streamlit app:

```bash
streamlit run app.py
```

2. Open your web browser and navigate to `http://localhost:8501`

3. Use the sidebar to configure settings:

   - Adjust confidence threshold
   - Toggle image enhancement
   - Enable/disable email notifications
   - Switch between dark/light mode

4. Upload MRI scans for analysis:
   - Supported formats: JPG, JPEG, PNG
   - Recommended resolution: 150x150 pixels or higher
   - Clear, focused MRI scans (axial view preferred)

## Features in Detail

### Single Image Analysis

- Upload individual MRI scans
- View original and enhanced images
- Get detailed analysis with confidence scores
- Download PDF reports

### Batch Processing

- Process multiple images at once
- View batch analysis summary
- Export results in CSV/Excel format

### Analytics Dashboard

- Track analysis history
- View trends and patterns
- Generate statistical reports

### Image Comparison

- Compare multiple MRI scans
- Side-by-side analysis
- Comparative visualization

## System Requirements

- Python 3.8 or higher
- 4GB RAM minimum (8GB recommended)
- Modern web browser
- Internet connection (for email notifications)

## File Structure

```
brain-tumor-detection/
│
├── app.py                  # Main application file
├── requirements.txt        # Python dependencies
├── README.md              # Project documentation
│
├── brain_tumor_model_quantized.tflite    # TFLite model file
│
├── results/               # Directory for saved results
│   └── ...
│
└── assets/               # Application assets
    └── ...
```

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Create a Pull Request

## Security and Privacy

- No patient data is stored permanently
- All processing is done locally
- Optional email notifications are sent securely
- Reports can be password protected

## Troubleshooting

Common issues and solutions:

1. Model loading error:

   - Verify model file exists in correct location
   - Check TensorFlow installation
   - Ensure correct Python version

2. Image processing error:

   - Check image format and size
   - Ensure sufficient memory
   - Try image enhancement option

3. Performance issues:
   - Close other resource-intensive applications
   - Reduce batch size for multiple images
   - Update graphics drivers

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- TensorFlow team for TFLite support
- Streamlit for the web framework
- OpenCV for image processing
- Scientific Python community

## Contact

For questions and support, please open an issue in the GitHub repository or contact [your-email@example.com]

## Version History

- 1.0.0: Initial release with TFLite support
- 1.1.0: Added batch processing
- 1.2.0: Enhanced reporting and analytics
- 1.3.0: Added image comparison features

---

**Note**: This application is for research and educational purposes only. It should not be used as the sole basis for medical decisions. Always consult with qualified healthcare professionals for proper diagnosis and treatment.
