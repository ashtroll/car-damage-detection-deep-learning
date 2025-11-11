# Contributing to Car Damage Detection

Thank you for considering contributing to this project! 🚗

## How to Contribute

### Reporting Bugs
- Use GitHub Issues to report bugs
- Include:
  - Python version
  - OS (Windows/Linux/macOS)
  - Steps to reproduce
  - Expected vs actual behavior
  - Error messages/screenshots

### Suggesting Enhancements
- Open an issue with the `enhancement` label
- Describe the feature and its benefits
- Provide examples if possible

### Pull Requests

1. **Fork the repository**
   ```bash
   git clone https://github.com/YOUR_USERNAME/car-damage-detection-deep-learning.git
   cd car-damage-detection-deep-learning
   ```

2. **Create a feature branch**
   ```bash
   git checkout -b feature/your-feature-name
   ```

3. **Set up environment**
   ```bash
   conda create -n car-damage python=3.12
   conda activate car-damage
   pip install -r requirements.txt
   ```

4. **Make your changes**
   - Follow existing code style
   - Add comments for complex logic
   - Update documentation if needed

5. **Test your changes**
   - Ensure the app runs: `python damage_detection_app/app.py`
   - Test training notebooks if modified
   - Check for any breaking changes

6. **Commit with clear messages**
   ```bash
   git add .
   git commit -m "feat: add confidence threshold slider to GUI"
   ```

7. **Push and create PR**
   ```bash
   git push origin feature/your-feature-name
   ```
   Then open a Pull Request on GitHub with:
   - Clear title and description
   - Reference related issues
   - Screenshots/GIFs if UI changes

## Code Style Guidelines

- **Python**: Follow PEP 8
- **Docstrings**: Use clear, concise descriptions
- **Naming**: Use descriptive variable names
- **Imports**: Group standard lib, third-party, local imports

## Areas for Contribution

- 🎨 **GUI Enhancements**: Add features like confidence sliders, batch export
- 📊 **Visualization**: Improve metrics plotting
- 🚀 **Performance**: Optimize inference speed
- 📝 **Documentation**: Improve README, add tutorials
- 🧪 **Testing**: Add unit tests
- 🌐 **Web Interface**: Create a web version with FastAPI
- 📦 **Deployment**: Docker containerization, cloud deployment guides

## Support
- 📫 Open an [issue](https://github.com/ashtroll/car-damage-detection-deep-learning/issues)
- 💬 Start a [discussion](https://github.com/ashtroll/car-damage-detection-deep-learning/discussions)

Thank you for helping improve this project! 🙏
