# Build Instructions

This document provides detailed instructions for building Dark World for different platforms.

## Prerequisites

- Unity 2022.3 LTS or newer
- Platform-specific SDKs (if building for mobile)

## Development Build

1. Open the project in Unity
2. Go to `File → Build Settings`
3. Select your target platform
4. Add scenes from `Assets/Scenes/` folder:
   - MainMenu.unity
   - Level01.unity
   - (Add other levels as they are created)
5. Set "Development Build" checkbox for debugging
6. Click "Build and Run"

## Release Build

### Windows Standalone

1. `File → Build Settings`
2. Select "PC, Mac & Linux Standalone"
3. Set Target Platform to "Windows"
4. Set Architecture to "x86_64"
5. Uncheck "Development Build"
6. Go to `Player Settings`:
   - Set Company Name
   - Set Product Name to "Dark World"
   - Set Version number
   - Configure icon and splash screen
7. Click "Build"

### Mac Standalone

1. Follow Windows steps but select "Mac OSX" as Target Platform
2. Set Architecture to "Apple Silicon" for M1/M2 Macs or "Intel 64-bit" for Intel Macs

### Linux Standalone

1. Follow Windows steps but select "Linux" as Target Platform
2. Set Architecture to "x86_64"

## Optimization Settings

### For Release Builds:
- Disable "Development Build"
- Set "Scripting Backend" to IL2CPP (for better performance)
- Enable "Engine code stripping"
- Optimize graphics settings based on target platform

### Player Settings Checklist:
- [ ] Company Name set
- [ ] Product Name set to "Dark World"
- [ ] Version number updated
- [ ] Icon configured (multiple sizes)
- [ ] Splash screen configured
- [ ] Default cursor set (if custom)
- [ ] Resolution settings appropriate

## Platform-Specific Notes

### Windows
- Consider code signing for distribution
- Test on different Windows versions
- Include Visual C++ Redistributables if needed

### Mac
- May require developer signing for distribution
- Test on both Intel and Apple Silicon if possible

### Linux
- Test on major distributions (Ubuntu, Fedora, etc.)
- Consider AppImage for easy distribution

## Distribution

### Steam
- Follow Steam partner documentation
- Include Steam SDK integration
- Configure achievements and trading cards

### Itch.io
- Build for multiple platforms
- Include good screenshots and description
- Consider web build for browser play

## Troubleshooting

### Common Build Issues:
- **Missing scenes**: Ensure all scenes are added to build settings
- **Asset references**: Check for missing script references
- **Platform compatibility**: Verify all assets work on target platform
- **Performance**: Profile builds to identify bottlenecks

### Performance Tips:
- Use sprite atlases to reduce draw calls
- Optimize audio compression settings
- Remove unused assets before building
- Use object pooling for frequently spawned objects