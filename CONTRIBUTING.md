# Contributing to InstructDojo

Guidelines for contributing to the InstructDojo instruction engineering repository.

## Contribution Process

### Creating New Instruction Sets

1. **Use PROMPTCRAFT INSTRUCTION SPECIALIST**
   - Initialize with [promptcraft_instruction_specialist.md](promptcraft-specialist/promptcraft_instruction_specialist.md)
   - Request `output_format: complete_package`
   - Ensure CODEAI style compliance

2. **Directory Structure**
   ```
   [name]-instructions/
   ├── README.md                    # Documentation
   └── [name]_[variant].md          # Instruction file
   ```

3. **Required Components**
   - Identity statement with "highly skilled"
   - CRITICAL RULES section
   - CAPABILITIES with ==== separators
   - RESPONSE METHODOLOGY
   - RULES and OBJECTIVE sections

4. **Testing Requirements**
   - Verify with 3+ different AI models
   - Document performance metrics
   - Confirm no initialization response
   - Test edge cases and error handling

5. **Pull Request**
   - Fork repository, create feature branch
   - Include test results and metrics
   - Update main README.md integration
   - Follow PR template

### Improving Existing Instructions

1. **Performance Optimization**
   - Measure current performance
   - Implement improvements
   - Document metric changes
   - Maintain backward compatibility

2. **Security Enhancements**
   - Identify vulnerabilities
   - Apply fixes with testing
   - Document security improvements
   - Follow OWASP guidelines

3. **Technical Updates**
   - Update deprecated patterns
   - Add new capabilities
   - Improve error handling
   - Enhance documentation

## Quality Standards

### Mandatory Requirements

**Technical Accuracy**
- Domain expertise verification ✓
- Terminology correctness ✓
- Method validity ✓
- Safety implementation ✓

**CODEAI Style Compliance**
- Direct technical communication ✓
- No conversational tone ✓
- Complete deliverables only ✓
- Structured sections with ==== ✓

**Performance Metrics**
- Response time optimization
- Token efficiency
- Error rate < 0.1%
- Cross-model compatibility

**Documentation Standards**
- Complete README.md
- Usage examples (3+ minimum)
- Technical specifications
- Integration instructions

## Instruction Engineering Standards

### Framework Components
```markdown
You are [NAME], a highly skilled [domain] specialist...

## CRITICAL RULES
1. **[Rule]** - [explanation]
2. **[Rule]** - [explanation]

====

CAPABILITIES

[Technical description]

====

RESPONSE METHODOLOGY

## 1. [STAGE]
[Process description]

====

[DOMAIN-SPECIFIC SECTIONS]

====

RULES

- [Operational rules]

====

OBJECTIVE

[Clear purpose statement]
```

### Style Guidelines

**Language**
- Technical precision required
- No pleasantries or fluff
- Direct actionable statements
- Measurable outcomes

**Structure**
- Consistent formatting
- Clear section separation
- Logical flow
- No redundancy

## Testing Protocol

### Required Testing

1. **Functionality Testing**
   ```
   Models to test:
   - Claude 3 Opus/Sonnet
   - GPT-4/GPT-3.5
   - Open source alternatives
   
   Metrics to track:
   - Instruction compliance rate
   - Output quality score
   - Error frequency
   - Performance timing
   ```

2. **Edge Case Testing**
   - Invalid inputs
   - Boundary conditions
   - Error scenarios
   - Recovery testing

3. **Performance Testing**
   - Response time measurement
   - Token usage optimization
   - Consistency verification
   - Scalability assessment

### Test Documentation
```markdown
## Test Results

### Model: [Name]
- Compliance: [%]
- Quality: [1-10]
- Errors: [count]
- Avg Response: [ms]

### Edge Cases
- [Scenario]: [Result]
- [Scenario]: [Result]

### Performance
- Baseline: [metric]
- Optimized: [metric]
- Improvement: [%]
```

## Pull Request Requirements

### PR Template
```markdown
## Type
- [ ] New Instruction Set
- [ ] Improvement
- [ ] Bug Fix
- [ ] Documentation

## Changes
[Technical description of changes]

## Testing
[Test results summary]

## Metrics
- Performance impact: [%]
- Quality improvement: [score]
- Error reduction: [%]

## Integration
- [ ] README.md updated
- [ ] Directory structure correct
- [ ] Links verified
- [ ] Style compliance checked
```

### Review Criteria

**Technical Review**
- Code quality assessment
- Performance verification
- Security validation
- Style compliance

**Documentation Review**
- Completeness check
- Example quality
- Integration accuracy
- Link validation

## Contribution Standards

### Do's
- Follow CODEAI style strictly
- Include measurable improvements
- Test thoroughly before submitting
- Document all changes clearly
- Use PROMPTCRAFT INSTRUCTION SPECIALIST

### Don'ts
- No conversational instructions
- No initialization messages
- No incomplete submissions
- No untested changes
- No style deviations

## Review Process

1. **Automated Checks**
   - Style compliance verification
   - Link validation
   - Format checking
   - Structure validation

2. **Technical Review**
   - Domain expertise verification
   - Performance assessment
   - Security evaluation
   - Quality metrics

3. **Final Approval**
   - Maintainer review
   - Integration testing
   - Documentation verification
   - Merge decision

## Support

- **Questions**: Open a discussion
- **Issues**: Use issue templates
- **Help**: Check existing documentation
- **Contact**: Via GitHub discussions

---

**Engineering excellence through collaborative improvement**
