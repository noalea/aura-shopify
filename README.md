# Aura Shopify Theme

A custom Shopify theme built with modern design and functionality.

## Prerequisites

Before you begin, ensure you have the following installed:

- **Shopify CLI** - [Installation Guide](https://shopify.dev/docs/themes/tools/cli/install)
- **Node.js** (v18 or higher recommended)
- **A Shopify Partner Account** or access to a Shopify store
- **Git** (for version control)

## Getting Started

### 1. Clone the Repository

```bash
git clone <repository-url>
cd auraShopify
```

### 2. Set Up Environment Variables

Copy the example environment file and configure it:

```bash
cp .env-example .env
```

Edit the `.env` file and add your Shopify store information:

```
SHOPIFY_FLAG_STORE=your-store-name.myshopify.com
```

Replace `your-store-name` with your actual Shopify store name.

### 3. Install Shopify CLI

If you haven't installed Shopify CLI yet, follow these steps:

**macOS (using Homebrew):**
```bash
brew tap shopify/shopify
brew install shopify-cli
```

**Windows (using RubyGems):**
```bash
gem install shopify-cli
```

**Linux:**
```bash
gem install shopify-cli
```

Verify the installation:
```bash
shopify version
```

### 4. Authenticate with Shopify

Log in to your Shopify Partner account or store:

```bash
shopify auth logout  # Optional: logout if switching accounts
shopify login --store your-store-name.myshopify.com
```

Follow the prompts to authenticate through your browser.

## Running the Theme Locally

### Development Mode

To start a local development server and preview your theme:

```bash
shopify theme dev
```

This command will:
- Upload your theme to Shopify as a development theme
- Start a local server (typically at `http://127.0.0.1:9292`)
- Watch for file changes and automatically sync them
- Open your browser to preview the theme

**Options:**
- `--store=your-store-name.myshopify.com` - Specify a different store
- `--theme=THEME_ID` - Use a specific theme ID
- `--host=HOST` - Specify the host URL (default: 127.0.0.1)
- `--port=PORT` - Specify the port (default: 9292)

### Live Reload

The development server includes live reload functionality. When you make changes to:
- `.liquid` files (templates, sections, snippets)
- `.css` files
- `.js` files

The browser will automatically refresh to show your changes.

## Project Structure

```
auraShopify/
├── assets/           # CSS, JavaScript, and image files
├── blocks/           # Theme blocks (app blocks)
├── config/           # Theme settings and configuration
├── layout/           # Layout templates
├── locales/          # Translation files
├── sections/         # Theme sections
├── snippets/         # Reusable code snippets
└── templates/        # Page templates
```

## Common Commands

### Push Theme to Shopify
```bash
shopify theme push
```

### Pull Theme from Shopify
```bash
shopify theme pull
```

### Publish Theme
```bash
shopify theme publish
```

### Check Theme for Issues
```bash
shopify theme check
```

### Package Theme for Upload
```bash
shopify theme package
```

## Development Workflow

1. **Start Development Server**
   ```bash
   shopify theme dev
   ```

2. **Make Changes**
   - Edit files in `sections/`, `snippets/`, `templates/`, or `assets/`
   - Changes will automatically sync to your development theme

3. **Preview Changes**
   - View changes in your browser at the provided URL
   - Test on different devices using the local network URL

4. **Commit Changes**
   ```bash
   git add .
   git commit -m "Description of changes"
   git push
   ```

## Troubleshooting

### Authentication Issues
If you encounter authentication problems:
```bash
shopify auth logout
shopify login --store your-store-name.myshopify.com
```

### Port Already in Use
If port 9292 is already in use, specify a different port:
```bash
shopify theme dev --port=9293
```

### File Sync Issues
If files aren't syncing properly:
1. Stop the development server (Ctrl+C)
2. Clear the local cache
3. Restart the server

### Permission Errors
Ensure you have the necessary permissions on the Shopify store:
- Theme editing permissions
- App development permissions (if using app blocks)

## Resources

- [Shopify Theme Documentation](https://shopify.dev/docs/themes)
- [Shopify CLI Documentation](https://shopify.dev/docs/themes/tools/cli)
- [Liquid Reference](https://shopify.dev/docs/api/liquid)
- [Theme Architecture](https://shopify.dev/docs/themes/architecture)

## Support

For issues or questions:
1. Check the [Shopify Community Forums](https://community.shopify.com/)
2. Review the [Shopify Theme Documentation](https://shopify.dev/docs/themes)
3. Contact the development team

## License

[Add your license information here]
