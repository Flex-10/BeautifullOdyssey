# Contributing to BeautifullOdyssey

Thank you for your interest in contributing to BeautifullOdyssey! This document provides guidelines for contributing to this RimWorld mod.

## Getting Started

### Prerequisites

- RimWorld 1.6+ with Odyssey DLC
- Basic understanding of RimWorld modding
- Text editor for XML editing

### Development Setup

1. Fork the repository
2. Clone your fork locally
3. Make changes to the XML files
4. Test in RimWorld
5. Submit a pull request

## Types of Contributions

### Beauty Value Adjustments

The most common type of contribution. When suggesting beauty value changes:

1. **Test in-game first** - Load the mod and check current values
2. **Provide reasoning** - Why should the value be changed?
3. **Consider balance** - How does this affect gameplay?
4. **Update documentation** - Change the README.md table accordingly

### New Building Support

To add support for new Odyssey buildings:

1. **Check the building exists** - Verify it's part of the Odyssey DLC
2. **Determine appropriate value** - Consider the building's role and appearance
3. **Add patch operation** - Follow existing patterns in `OdysseyBeautyPatch.xml`
4. **Update README** - Add to the features table

### Bug Fixes

When fixing bugs:

1. **Reproduce the issue** - Confirm the bug exists
2. **Identify root cause** - Check XML syntax, patch operations, etc.
3. **Test the fix** - Ensure it works without breaking other features
4. **Document the change** - Explain what was wrong and how you fixed it

## Code Standards

### XML Formatting

- Use consistent indentation (2 spaces)
- Include comments for each building patch
- Follow existing naming conventions

Example patch operation:

```xml
<!-- BuildingName: X (description of change) -->
<Operation Class="PatchOperationReplace">
    <xpath>/Defs/ThingDef[defName="BuildingName"]/statBases/Beauty</xpath>
    <value>
        <Beauty>X</Beauty>
    </value>
</Operation>
```

### Beauty Value Guidelines

- **Positive values only** - This mod turns ugly buildings beautiful
- **Balanced progression** - More important buildings should have higher values
- **Reasonable ranges** - Typically 5-20 for most buildings
- **Consider original values** - Usually flip negative to positive equivalent

Current value ranges:

- **Basic buildings**: 5-10 (GravAnchor, GravcorePowerCell)
- **Standard buildings**: 10 (most buildings)
- **Special buildings**: 15-20 (GravEngine gets highest values)

## Testing Guidelines

### Basic Testing

Before submitting any changes:

1. **Load test** - Mod loads without errors
2. **Value verification** - Beauty values appear correctly in building info
3. **Save compatibility** - Existing saves still work

### Extended Testing

For more thorough testing:

1. **Fresh colony** - Start new game and build all affected buildings
2. **Multiple scenarios** - Test in different game situations
3. **Mod list testing** - Test with your typical mod setup
4. **Performance** - Ensure no lag or performance issues

## Submitting Changes

### Pull Request Process

1. **Create descriptive branch name** - e.g., `adjust-gravengine-beauty` or `fix-signaljammer-patch`
2. **Make focused changes** - One feature/fix per PR
3. **Update README if needed** - Keep documentation current
4. **Fill out PR template** - Provide all requested information
5. **Respond to feedback** - Address review comments promptly

### Commit Messages

Use clear, descriptive commit messages:

- `Adjust GravEngine beauty value from +10 to +15`
- `Fix PatchOperationReplace for SignalJammer`
- `Add support for NewOdysseyBuilding`

## Beauty Value Philosophy

This mod follows these principles:

### Design Goals

- **Make ugly buildings beautiful** - Convert negative beauty to positive
- **Maintain game balance** - Don't make buildings overpowered aesthetically
- **Reflect building importance** - More critical buildings = higher beauty
- **Stay lore-friendly** - Advanced technology should look impressive

### Value Assignment Logic

- **GravEngine**: Highest values (15-20) - The heart of gravship technology
- **Shield/Field equipment**: High values (10-15) - Advanced defensive tech
- **Support buildings**: Medium values (8-12) - Important but secondary
- **Basic components**: Lower values (5-10) - Functional but not spectacular

## Getting Help

### Questions?

- **Open an issue** with the "question" label
- **Check existing issues** - Your question might already be answered
- **Review the README** - Basic information is documented there

### Problems?

- **Bug reports** - Use the bug report template
- **Feature requests** - Use the feature request template
- **Documentation issues** - Open a regular issue

## Recognition

Contributors will be:

- Listed in release notes for their contributions
- Mentioned in the mod description (for significant contributions)
- Given credit in commit messages and PR descriptions

Thank you for helping make BeautifullOdyssey better! 🚀
