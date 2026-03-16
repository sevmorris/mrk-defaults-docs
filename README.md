# mrk defaults.sh Reference Documentation

A comprehensive, searchable reference guide for the macOS defaults configured by the [mrk bootstrap system](https://github.com/sevmorris/mrk).

## Features

- 📖 **Comprehensive Documentation** - Detailed descriptions of every default setting
- 🔍 **Searchable Interface** - Find specific settings quickly
- 📋 **Copy Commands** - One-click copying of `defaults write` commands
- 📱 **Responsive Design** - Works on desktop, tablet, and mobile
- 🎨 **Technical Documentation Style** - Clean, professional presentation
- 🔄 **Auto-parsing** - Automatically generates documentation from `defaults.sh`

## Usage

### GitHub Pages Deployment

1. Fork or clone this repository
2. Enable GitHub Pages in repository settings
3. Point to `main` branch
4. Access at `https://yourusername.github.io/mrk-defaults-docs/`

### Local Development

```bash
# Clone the repository
git clone https://github.com/sevmorris/mrk-defaults-docs.git
cd mrk-defaults-docs

# Serve locally (requires Python 3)
python3 -m http.server 8000

# Or with Node.js
npx serve .

# Open http://localhost:8000 in your browser
```

## Structure

- `index.html` - Main documentation page
- `style.css` - Technical documentation styling
- `script.js` - Parser and interactive functionality
- `defaults.sh` - Source script (copied from mrk)

## How It Works

The JavaScript parser reads the `defaults.sh` script and:

1. **Extracts sections** from banner comments
2. **Parses `write_default` commands** to extract domain, key, type, and value
3. **Maps to detailed descriptions** using a comprehensive description database
4. **Generates searchable HTML** with copy-able commands
5. **Provides navigation** and filtering capabilities

## Adding Descriptions

The `DEFAULT_DESCRIPTIONS` object in `script.js` contains detailed explanations for each setting. To add or improve descriptions:

```javascript
'domain.key': {
    title: 'Human-readable name',
    description: 'Detailed explanation of what this setting does...',
    category: 'Category name'
}
```

## Contributing

1. Fork the repository
2. Add or improve setting descriptions in `script.js`
3. Test locally to ensure parsing works correctly
4. Submit a pull request

## License

MIT License - see LICENSE file for details.

## Related

- [mrk bootstrap system](https://github.com/sevmorris/mrk) - The source of the defaults.sh script
- [macOS defaults reference](https://macos-defaults.com/) - Additional macOS defaults documentation