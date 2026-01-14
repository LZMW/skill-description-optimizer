# Contributing to Skill Description Optimizer

First off, thank you for considering contributing to Skill Description Optimizer! It's people like you that make the open-source community such a great place to learn and inspire.

## Code of Conduct

By participating in this project, you agree to abide by our code of conduct:
- Be respectful and inclusive
- Provide constructive feedback
- Focus on what is best for the community
- Show empathy towards other community members

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check existing issues to avoid duplicates. When you create a bug report, include as many details as possible:

**Bug Report Template**

```markdown
**Description**
A clear and concise description of what the bug is.

**To Reproduce**
Steps to reproduce the behavior:
1. Go to '...'
2. Click on '....'
3. Scroll down to '....'
4. See error

**Expected Behavior**
A clear and concise description of what you expected to happen.

**Screenshots**
If applicable, add screenshots to help explain your problem.

**Environment:**
- OS: [e.g. Windows 10, macOS 12.0]
- Claude Code Version: [e.g. 1.0.0]
- Skill Version: [e.g. 1.0.0]

**Additional Context**
Add any other context about the problem here.
```

### Suggesting Enhancements

Enhancement suggestions are tracked as GitHub issues. When creating an enhancement suggestion, include:
- Use a clear and descriptive title
- Provide a detailed description of the suggested enhancement
- Explain why this enhancement would be useful
- List some examples of how this feature would be used

### Pull Requests

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

**Pull Request Checklist**

- [ ] My code follows the style guidelines of this project
- [ ] I have performed a self-review of my own code
- [ ] I have commented my code, particularly in hard-to-understand areas
- [ ] I have made corresponding changes to the documentation
- [ ] My changes generate no new warnings
- [ ] I have tested my changes locally
- [ ] I have added tests that prove my fix is effective or that my feature works

## Development Setup

1. Fork and clone the repository
2. Ensure you have Claude Code CLI with Agent SDK installed
3. Copy the skill to your local skills directory:

```bash
cp -r skill-description-optimizer ~/.claude/skills/
```

4. Test the skill by asking Claude to optimize a skill description

## Coding Standards

- Follow existing code style and formatting
- Use clear and descriptive variable/function names
- Add comments for complex logic
- Keep functions focused and modular
- Write meaningful commit messages

## Documentation

If you're adding new features or changing existing ones, please update the documentation:
- README.md for user-facing changes
- SKILL.md for skill behavior changes
- references/best_practices.md for technique updates
- CHANGELOG.md for version history

## Testing

Test your changes thoroughly:
- Verify the skill works with various skill descriptions
- Check that optimization quality meets SDS standards
- Ensure no conflicts with existing skills
- Validate that all quality checks pass

## Questions?

Feel free to open an issue for any questions about contributing or the project in general.

---

Thank you for your contributions! 🎉
