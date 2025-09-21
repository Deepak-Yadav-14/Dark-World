# Contributing to Dark World

Thank you for your interest in contributing to Dark World! This document provides guidelines for contributing to this Unity 2D platformer project.

## 🚀 Getting Started

1. **Fork the repository** on GitHub
2. **Clone your fork** to your local machine
3. **Set up the development environment** by opening the project in Unity 2022.3 LTS or newer
4. **Create a new branch** for your feature or bug fix

## 🛠️ Development Setup

### Prerequisites
- Unity 2022.3 LTS or newer
- Git
- Visual Studio or Visual Studio Code (recommended for C# development)

### Project Structure
- `Assets/Scripts/` - All C# scripts organized by functionality
- `Assets/Scenes/` - Unity scenes
- `Assets/Sprites/` - 2D artwork and textures
- `Assets/Audio/` - Sound effects and music
- `Assets/Prefabs/` - Reusable GameObjects

## 📝 Coding Standards

### C# Guidelines
- Follow Microsoft C# naming conventions
- Use PascalCase for public members and methods
- Use camelCase for private fields
- Prefix private fields with underscore (e.g., `_playerHealth`)
- Add XML documentation for public APIs

```csharp
/// <summary>
/// Handles player movement and input
/// </summary>
public class PlayerController : MonoBehaviour
{
    [SerializeField] private float _moveSpeed = 5f;
    [SerializeField] private float _jumpForce = 10f;
    
    /// <summary>
    /// Gets or sets the player's current health
    /// </summary>
    public int Health { get; set; }
    
    private void Update()
    {
        HandleMovement();
    }
}
```

### Unity Guidelines
- Use SerializeField for inspector-visible private fields
- Organize scripts with regions for better readability
- Cache component references in Start() or Awake()
- Use object pooling for frequently instantiated objects
- Optimize for mobile performance when possible

## 🎯 Types of Contributions

### Bug Fixes
- Check existing issues before creating new ones
- Include steps to reproduce the bug
- Test your fix thoroughly

### New Features
- Discuss major features in an issue first
- Keep features focused and well-documented
- Include appropriate tests when possible

### Art Assets
- Follow the existing art style
- Ensure sprites are properly sized (pixels per unit)
- Include source files when possible (.psd, .aseprite, etc.)

### Audio
- Use appropriate file formats (OGG Vorbis preferred)
- Maintain consistent audio levels
- Include uncompressed source files when possible

## 🔄 Submission Process

1. **Create a branch** from main: `git checkout -b feature/your-feature-name`
2. **Make your changes** following the coding standards
3. **Test thoroughly** in Unity Editor and builds
4. **Commit with clear messages**:
   ```
   feat: add double jump ability
   
   - Implemented double jump mechanic for player
   - Added animation for double jump
   - Updated player controller with jump count tracking
   ```
5. **Push to your fork**: `git push origin feature/your-feature-name`
6. **Create a Pull Request** with:
   - Clear title and description
   - Screenshots/GIFs for visual changes
   - Testing notes

## 🧪 Testing Guidelines

### Before Submitting
- [ ] Test in Unity Editor
- [ ] Build and test on target platforms
- [ ] No console errors or warnings
- [ ] Performance impact assessed
- [ ] Code follows project standards

### Testing Checklist for Features
- [ ] Feature works as intended
- [ ] Doesn't break existing functionality
- [ ] Handles edge cases appropriately
- [ ] Performance is acceptable
- [ ] UI/UX is intuitive

## 📋 Issue Guidelines

### Bug Reports
Please include:
- Unity version
- Platform (Windows/Mac/Linux)
- Steps to reproduce
- Expected vs actual behavior
- Screenshots/videos if applicable
- Console error messages

### Feature Requests
Please include:
- Clear description of the feature
- Use cases and benefits
- Potential implementation approach
- Mockups or references if applicable

## 🎮 Game Design Considerations

When contributing gameplay features:
- Maintain the game's challenging but fair difficulty
- Ensure new mechanics fit the dark/atmospheric theme
- Consider accessibility and different skill levels
- Test with various input methods

## 🤝 Community Guidelines

- Be respectful and constructive in discussions
- Help newcomers and answer questions
- Provide detailed feedback on pull requests
- Celebrate others' contributions

## 📞 Questions?

If you have questions about contributing:
- Open an issue for discussion
- Check existing documentation
- Reach out to maintainers

Thank you for contributing to Dark World! 🌙