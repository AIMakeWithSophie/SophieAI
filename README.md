# Sophie AI

<div align="center">
  <img src="https://github.com/user-attachments/assets/d118a92d-82dd-48a1-83cc-7fa293552910" alt="Sophie AI Banner" width="40%" />
</div>

<div align="center">

📄 [Technical Report](https://arxiv.org/pdf/sophie-ai) | 📖 [Documentation](https://www.makewithsophie.xyz/) | 💡 [Examples](https://github.com/makewithsophie/sophieai)

</div>

## README Translations

[中文说明](i18n/readme/README_CN.md) | [日本語の説明](i18n/readme/README_JA.md) | [한국어 설명](i18n/readme/README_KOR.md) | [Persian](i18n/readme/README_FA.md) | [Français](i18n/readme/README_FR.md) | [Português](i18n/readme/README_PTBR.md) | [Türkçe](i18n/readme/README_TR.md) | [Русский](i18n/readme/README_RU.md) | [Español](i18n/readme/README_ES.md) | [Italiano](i18n/readme/README_IT.md) | [ไทย](i18n/readme/README_TH.md) | [Deutsch](i18n/readme/README_DE.md) | [Tiếng Việt](i18n/readme/README_VI.md) | [עִברִית](i18n/readme/README_HE.md) | [Tagalog](i18n/readme/README_TG.md) | [Polski](i18n/readme/README_PL.md) | [Arabic](i18n/readme/README_AR.md) | [Hungarian](i18n/readme/README_HU.md) | [Srpski](i18n/readme/README_RS.md) | [Română](i18n/readme/README_RO.md) | [Nederlands](i18n/readme/README_NL.md) | [Ελληνικά](i18n/readme/README_GR.md)

## Overview

Sophie is an AI-powered video generation platform that transforms text descriptions into high-quality videos. Powered by Google's Veo 3 technology, Sophie makes video creation accessible to everyone through natural language prompts.

## Key Features

- **Text-to-Video Generation** - Transform any text description into a video
- **Fast Processing** - Generate videos in 1-2 minutes
- **HD Quality** - Create videos in 1920x1080 resolution
- **Extended Duration** - Support for videos up to 60 seconds long
- **Multiple Styles** - Generate realistic or artistic video styles
- **Easy Integration** - Simple API for developers
- **Multi-Platform Support** - Works on web, mobile, and desktop
- **Production Ready** - Built for scale and reliability

## Video Tutorials

[Sophie AI Tutorial Series](https://www.youtube.com/watch?v=SophieAI&list=PLx5pnFXdPTRzWla0RaOxALTSTnVq53fKL)

## Use Cases

- **Content Creation** - Social media videos, marketing content
- **Educational Content** - Training videos, tutorials, presentations
- **Creative Projects** - Art installations, creative storytelling
- **Social Media** - Quick video content for platforms
- **Business Applications** - Product demos, explainer videos
- **Game Development** - Concept videos, trailers

## Quick Start

### Prerequisites

- [Python 3.8+](https://www.python.org/downloads/)
- [Node.js 18+](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)
- [pnpm](https://pnpm.io/installation)
- Google Cloud account with Veo 3 API access

> **Note for Windows Users:** [WSL 2](https://learn.microsoft.com/en-us/windows/wsl/install-manual) is recommended.

### Using the Starter Template (Recommended)

```bash
git clone https://github.com/makewithsophie/sophieai-starter.git
cd sophieai-starter
cp .env.example .env
pnpm i && pnpm build && pnpm start
```

### Manual Installation (For Development)

#### Download the Repository

```bash
# Clone the repository
git clone https://github.com/makewithsophie/sophieai.git

# Check out the latest stable release
git checkout $(git describe --tags --abbrev=0)
```

#### Configure Environment

Copy .env.example to .env and fill in the appropriate values.

```bash
cp .env.example .env
```

Required environment variables:
```env
GOOGLE_CLOUD_PROJECT_ID=your-project-id
VEO_3_API_KEY=your-veo-3-api-key
STORAGE_BUCKET=your-storage-bucket
```

#### Start the Application

```bash
pnpm i
pnpm build
pnpm start

# Clean project if needed
pnpm clean
```

### Web Interface

Once Sophie is running, open another terminal and start the client:

```bash
pnpm start:client
```

Follow the URL to start generating videos through the web interface.

Then read the [Documentation](https://www.makewithsophie.xyz/) to learn how to customize Sophie and create better prompts.

## API Usage

### Basic Video Generation

```javascript
const sophie = require('@makewithsophie/core');

const video = await sophie.generateVideo({
  prompt: "A golden retriever running through a green meadow on a sunny day",
  duration: 30, // seconds
  resolution: "1920x1080",
  style: "realistic"
});

console.log(video.downloadUrl);
```

### Advanced Configuration

```javascript
const video = await sophie.generateVideo({
  prompt: "Ocean waves crashing on a beach at sunset",
  duration: 60,
  resolution: "1920x1080",
  style: "cinematic",
  fps: 30,
  aspectRatio: "16:9",
  quality: "high"
});
```

## Video Specifications

| Feature | Details |
|---------|---------|
| Maximum Length | 60 seconds |
| Resolution | 1920x1080 (HD) |
| Generation Time | 1-2 minutes |
| File Format | MP4 |
| Frame Rate | 24-30 FPS |
| Aspect Ratios | 16:9, 4:3, 1:1 |

## Example Prompts

Here are examples of effective prompts for Sophie:

### Effective Prompts
- "A cat playing with a ball of yarn in a sunny living room with soft lighting"
- "Ocean waves crashing on a rocky beach at golden hour with seagulls flying overhead"
- "A person walking through a busy city street at night with neon lights reflecting on wet pavement"
- "Time-lapse of colorful flowers blooming in a spring garden with butterflies"

### Tips for Better Results

- **Be Specific** - Include details about lighting, colors, and mood
- **Describe Movement** - Mention if things should be moving slowly or quickly  
- **Set the Scene** - Tell Sophie where the action is happening
- **Keep It Simple** - One main idea per video works best
- **Use Descriptive Language** - Colors, textures, weather conditions
- **Specify Camera Angles** - Close-up, wide shot, aerial view, etc.

## Community & Contact

- [GitHub Issues](https://github.com/makewithsophie/sophieai/issues) - Report bugs and request features
- [Website](https://www.makewithsophie.xyz/) - Documentation and community resources

## Citation

If you use Sophie AI in your research, please cite our work:
```bibtex
@article{sophieai2025,
  title={Sophie AI: Democratizing Video Generation Through Natural Language},
  author={Sophie AI Team},
  journal={arXiv preprint arXiv:2501.xxxxx},
  year={2025}
}
```

## Contributors

<a href="https://github.com/makewithsophie/sophieai/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=makewithsophie/sophieai" alt="Sophie AI project contributors" />
</a>

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=makewithsophie/sophieai&type=Date)](https://star-history.com/#makewithsophie/sophieai&Date)

## System Requirements

### Minimum Requirements
- CPU: Quad-core processor
- RAM: 8GB
- Storage: 5GB free space
- Internet: Broadband (10 Mbps+ recommended)
- GPU: Optional but recommended for faster processing

### Software Requirements
- Python 3.8+
- Node.js 18+
- pnpm
- Git
- Google Cloud SDK (for API access)

### Recommended Specifications
- CPU: 8-core processor
- RAM: 16GB+
- Storage: 20GB+ SSD
- GPU: NVIDIA GTX 1060 or better
- Internet: 50 Mbps+ for optimal performance

## Project Structure
```
sophie/
├── packages/
│   ├── core/           # Core Sophie functionality
│   ├── api/            # API implementations
│   ├── web/            # Web interface
│   └── cli/            # Command-line interface
├── docs/              # Documentation
├── scripts/           # Utility scripts
├── examples/          # Example implementations
└── models/            # Model configurations
```

## Contributing

We welcome contributions to Sophie AI. Here's how you can help:

### Getting Started
1. Fork the repository
2. Create a new branch: `git checkout -b feature/your-feature-name`
3. Make your changes
4. Run tests: `pnpm test`
5. Submit a pull request

### Contribution Types
- Bug fixes
- New features  
- Documentation improvements
- Translations
- Test improvements
- UI/UX enhancements
- Example prompts and tutorials

### Development Guidelines
- Follow the existing code style
- Add comments for complex logic
- Update documentation for changes
- Add tests for new features
- Include example usage in documentation

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Privacy & Security

Sophie AI is committed to protecting user privacy:
- Generated videos are temporarily stored during processing
- No personal data is retained after video generation
- All API calls are encrypted
- Users retain full rights to their generated content

## Support

Need assistance? Here are your support options:

- **Documentation** - [https://www.makewithsophie.xyz/](https://www.makewithsophie.xyz/)
- **Issues** - [GitHub Issues](https://github.com/makewithsophie/sophieai/issues)
- **Email** - [support@makewithsophie.xyz](mailto:support@makewithsophie.xyz)

---

**Ready to create your first video with Sophie?** 

Get started now and transform your ideas into stunning videos.
