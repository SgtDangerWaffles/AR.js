# Contributing to AR.js

First off, thank you for considering contributing to AR.js! It's people like you that make AR.js such a great tool.

## Where do I go from here?

If you've noticed a bug or have a feature request, make sure to check our [Issues](https://github.com/AR-js-org/AR.js/issues) if there's something similar to what you have in mind. If not, feel free to create a new issue!

## Code of Conduct

This project and everyone participating in it is governed by our [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code.

## How Can I Contribute?

### Asking Questions and Getting Support

**Please don't use GitHub issues for general support questions.** GitHub issues are reserved for bug reports and feature requests.

If you have a question about using AR.js:

1. **Check the [FAQ](FAQ.md)** - Many common questions are already answered there
2. **Read the [Official Documentation](https://ar-js-org.github.io/AR.js-Docs/)** - Comprehensive guides and tutorials
3. **Search [StackOverflow](https://stackoverflow.com/search?q=ar.js)** - Many questions have already been answered
4. **Ask on [Gitter](https://gitter.im/AR-js/Lobby)** - Real-time chat with the community
5. **Search [old AR.js repository issues](https://github.com/jeromeetienne/AR.js/issues)** - Valuable information in closed issues

### Reporting Bugs

Before creating a bug report, please check existing issues to avoid duplicates.

**When filing a bug report, include:**

- A clear and descriptive title
- Exact steps to reproduce the problem
- Expected behavior vs actual behavior
- Browser version, OS, and device information
- Screenshots or code samples if applicable
- Links to a live demo (CodePen, Glitch, etc.) demonstrating the issue

Use the [Issue Template](ISSUE_TEMPLATE.md) when creating your issue.

### Suggesting Features

Feature requests are welcome! Before suggesting a feature:

1. Check if it's already been suggested in open/closed issues
2. Consider if it fits AR.js's scope and philosophy
3. Provide detailed use cases and rationale

**When suggesting a feature:**

- Use a clear and descriptive title
- Provide a detailed description of the suggested enhancement
- Explain why this feature would be useful to most users
- List any similar features in other projects if applicable

### Pull Requests

**⚠️ Important: All PRs must be made against the `dev` branch, not `master`.**

Ready to contribute code? Here's how:

1. **Fork the repository** and create your branch from `dev`
2. **Make your changes** following the coding style of the project
3. **Test your changes** on actual devices (specify which devices in PR)
4. **Ensure you haven't broken anything** - test existing functionality
5. **Update documentation** if you're adding/changing features
6. **Create a Pull Request** using our [PR Template](PULL_REQUEST_TEMPLATE.md)

#### Development Setup

```bash
# Clone your fork
git clone https://github.com/YOUR-USERNAME/AR.js.git
cd AR.js

# Add upstream remote
git remote add upstream https://github.com/AR-js-org/AR.js.git

# Create a branch from dev
git checkout dev
git checkout -b your-feature-branch

# Make your changes
# ...

# Build the project (if applicable)
make build

# Commit your changes
git add .
git commit -m "Your descriptive commit message"

# Push to your fork
git push origin your-feature-branch
```

#### Coding Guidelines

- Follow the existing code style
- Write clear, readable code
- Comment complex logic
- Keep changes focused and minimal
- Write [good commit messages](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)

#### Testing Your Changes

Before submitting a PR:

- Test on real devices, not just desktop browsers
- Test on both iOS and Android if possible
- Test in different lighting conditions (for AR features)
- Verify no console errors
- Check that examples still work

**In your PR, specify:**
- Device(s) tested on
- OS version(s)
- Browser(s) and version(s)

### Documentation

Documentation improvements are always welcome! This includes:

- Fixing typos or unclear wording
- Adding examples
- Improving the FAQ
- Writing tutorials

Documentation changes follow the same PR process but don't require extensive device testing.

## Project Structure

```
AR.js/
├── aframe/          # A-Frame components and builds
├── three.js/        # Three.js implementation
├── data/            # Markers, images, and other assets
│   └── marker-generator/  # Tools for creating markers
├── test/            # Test files
├── FAQ.md           # Frequently Asked Questions
├── README.md        # Main readme
└── CONTRIBUTING.md  # This file
```

## Recognition

Contributors will be recognized in release notes and we greatly appreciate all contributions, whether it's:

- Reporting a bug
- Discussing code improvements
- Submitting a fix
- Proposing new features
- Improving documentation

## Getting Help

If you need help with contributing:

- Check our [FAQ](FAQ.md)
- Ask in the [Gitter chat](https://gitter.im/AR-js/Lobby)
- Look at previous PRs for examples

## License

By contributing to AR.js, you agree that your contributions will be licensed under the same license as the project (MIT for AR.js code, LGPLv3 for jsartoolkit5 dependencies). See [LICENSE](LICENSE) for details.

---

Thank you for contributing to AR.js! 🎉
