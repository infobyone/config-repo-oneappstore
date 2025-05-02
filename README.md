# App Listing Repository for [Your Project Name]

Welcome! This repository is the central template for listing your application in the [Your Project Name] app store/catalog.

**Please DO NOT submit Pull Requests to this repository.** Instead, follow the steps below using your own fork.

## How to List Your App

1.  **Fork this Repository:** Click the "Fork" button at the top-right of this page to create your own copy under your GitHub account (e.g., `YourUsername/config-repo`).
2.  **Clone Your Fork:** Clone your newly created fork to your local machine:
    ```bash
    git clone https://github.com/YourUsername/config-repo.git
    cd config-repo
    ```
3.  **Create Your App's Config File:**
    * Inside the `apps/` directory, create a new subdirectory named *exactly* like your application's repository or fork name (e.g., `my-cool-app`).
    * Inside that new subdirectory, create a file named `config.one`.
    * The final path should look like: `apps/my-cool-app/config.one`
4.  **Edit `config.one`:** Fill this file with your app's details using the YAML format below. **All fields are required unless marked optional.**

    ```yaml
    # Required Fields:
    name: "My Cool App"             # The display name of your application.
    author: "Your Name or Org"             # author name.
    version: "1.2.3"                # Current version (must follow Semantic Versioning: MAJOR.MINOR.PATCH).
    description: "A brief description of what my cool app does." # Short and informative.
    logo_url: "https://your-domain.com/path/to/logo.png" # Direct HTTPS link to a logo image (e.g., PNG, JPG). Max ~512x512 recommended.
    download_url: "https://github.com/YourUsername/my-cool-app/releases/download/v1.2.3/my-cool-app.zip" # Direct HTTPS link to the downloadable file (e.g., zip, exe, apk).
    takedown: false                 # Set to `true` if you want to temporarily hide this app listing (e.g., outdated, broken). Defaults to shown (`false`).

    # Optional Fields:
    sha256sum: "a1b2c3d4..."        # (Highly Recommended) The SHA-256 hash (64 hex chars) of the file at download_url. Allows users to verify integrity. You can generate this using 'sha256sum <filename>' on Linux/macOS or 'Get-FileHash <filename> -Algorithm SHA256' in PowerShell.
    # homepage: "https://your-app-homepage.com" # Optional link to the app's website.
    # tags: ["utility", "game", "example"]  # Optional list of keywords/tags (client app might use these for filtering).
    ```

5.  **Commit and Push to Your Fork:** Save your `config.one` file, then commit and push the changes *only to your fork*:
    ```bash
    git add apps/your-app-name/config.one
    git commit -m "Add/Update My Cool App v1.2.3"
    git push origin main
    ```
6.  **Done!** Your app will be automatically picked up and listed in the [Your Project Name] client app during the next daily indexing run (typically around 2 PM IST / 8:30 AM UTC).

## Updating Your App Listing

To update your app's version, description, download URL, etc.:

1.  Edit the `config.one` file within your fork (`apps/your-app-name/config.one`).
2.  Commit and push the changes to your fork.
3.  The changes will appear after the next daily indexing run.

## Important Notes

* Ensure all URLs (`logo_url`, `download_url`) use **HTTPS**.
* Follow **Semantic Versioning** strictly for the `version` field.
* Keep the `description` concise.
* If you set `takedown: true`, your app will be hidden from the list but not removed from the index permanently (set back to `false` to reappear).
* To permanently remove your app, you can delete your fork or delete the `config.one` file within your fork (it will be removed from the index during the next run).

Thank you for contributing to [Your Project Name]!