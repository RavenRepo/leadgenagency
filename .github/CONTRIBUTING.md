# Contributing to LeadGenAgency

🎉 Thanks for your interest in contributing!

## How to Contribute

### 1. Report Issues
Found a bug or have a feature request? Open an issue with:
- Clear description of the issue
- Steps to reproduce (for bugs)
- Expected vs actual behavior

### 2. Submit Pull Requests
1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-agent`
3. Commit your changes: `git commit -m 'Add amazing new agent'`
4. Push: `git push origin feature/amazing-agent`
5. Open a Pull Request

### 3. Add New Agents
New agent? Follow the agent template:

```
agents/
└── [agent-name].md    # Follow schema in CLAUDE.md
```

Required sections:
- Role & Reports To
- Reads / Writes
- Human gate (yes/no)
- System Prompt
- Input Schema
- Output Schema
- Quality Criteria

### 4. Add New Skills
Skills live in `skills/`:
- `skills/[skill-name].md`
- Follow the pattern of existing skills
- Include: methodology, frameworks, benchmarks

### 5. Improve Benchmarks
Help grow the `knowledge/` wiki:
- Add real performance data
- Update conversion benchmarks
- Share proven formulas

## Quality Standards

- All agents must have quality criteria
- All workflows must have gate definitions
- README must stay current with structure changes
- CI checks must pass

## License

By contributing, you agree that your contributions will be licensed under the MIT License.