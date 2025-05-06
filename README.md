# App Listing Repository for [ONE APP STORE](https://oas-skyious.github.io)

Welcome to the ONE APP STORE app listing repository! This is the central template for listing your application in our app store. To maintain the integrity of the template and automate the listing process, we use forks instead of direct contributions. Please follow the steps below to list your app using your own fork.

**Important:** Do not submit Pull Requests to this repository. All changes should be made in your fork.

## How to List Your App

1. **Fork this Repository:**  
   Click the "Fork" button at the top-right of this page to create your own fork (e.g., `YourUsername/config-repo`).

2. **Clone Your Fork:**  
   Clone your fork to your local machine. Replace `YourUsername` with your GitHub username:
   ```bash
   git clone https://github.com/YourUsername/config-repo.git
   cd config-repo
   ```

3. **Create Your App's Config File:**  
   - In the `apps/` directory, create a subdirectory named **exactly** like your app's repository (e.g., `apps/my-cool-app/` for a repo named `my-cool-app`).  
   - Inside this subdirectory, create a file named `config.one`.  
   - Example path: `apps/my-cool-app/config.one`

4. **Edit `config.one`:**  
   Use the YAML format below to fill in your app's details. All fields are required unless marked optional.
   ```yaml
   name: "My Cool App"             # Display name of your app
   author: "Your Name or Org"      # Author name
   version: "1.2.3"                # Semantic Versioning (MAJOR.MINOR.PATCH)
   description: "A brief description of what my cool app does." # Max 100 characters
   logo_url: "https://your-domain.com/path/to/logo.png" # HTTPS link to logo (PNG/JPG, max 512x512)
   download_url: "https://github.com/YourUsername/my-cool-app/releases/download/v1.2.3/my-cool-app.zip" # HTTPS link to file
   takedown: false                 # Set to true to hide listing

   # Optional
   sha256sum: "a1b2c3d4..."        # SHA-256 hash for file verification
   homepage: "https://your-app-homepage.com" # App website
   tags: ["utility", "game"]       # Keywords for filtering
   ```

5. **Commit and Push to Your Fork:**  
   Save, commit, and push your changes:
   ```bash
   git add apps/my-cool-app/config.one
   git commit -m "Add My Cool App v1.2.3"
   git push origin main
   ```

6. **Done!**  
   Your app will be indexed and listed in the ONE APP STORE during the daily indexing run at **8 PM IST (2:30 PM UTC)**. The main ONE APP STORE website will update immediately after this run to reflect your app.

## Updating Your App Listing

To update your app:
1. Edit `config.one` in your fork (`apps/your-app-name/config.one`).
2. Commit and push the changes.
3. Updates will appear after the next indexing run at **8 PM IST**.

## Key Details

- **Indexing Time:** Occurs only at **8 PM IST (2:30 PM UTC)** daily. Changes made after this time will be indexed the next day.
- **Website Updates:** The main ONE APP STORE website updates every time after the index is updated, ensuring the latest listings are live.
- **URLs:** Must use **HTTPS**.
- **Versioning:** Follow [Semantic Versioning](https://semver.org/).
- **Takedown:** Use `takedown: true` to hide your app temporarily.
- **Removal:** Delete `config.one` or your fork to remove the app permanently.
- **Security:** Include `sha256sum` for file integrity verification.

## Additional Features

- **Multiple Apps:** Add more apps by creating additional subdirectories (e.g., `apps/app1/`, `apps/app2/`) with their own `config.one` files.
- **Logo Tips:** Use a square logo (recommended 512x512 pixels) for best results.
- **Download URL:** Must link directly to the file (e.g., GitHub release asset).

## Troubleshooting

- **App not listed?**  
  - Check `config.one` for correct format and required fields.
  - Ensure changes were pushed before **8 PM IST**.
  - Validate YAML syntax (use spaces, not tabs).

- **SHA-256 Hash:**  
  - Linux/macOS: `sha256sum <file>`
  - Windows (PowerShell): `Get-FileHash <file> -Algorithm SHA256`

Thank you for contributing to ONE APP STORE!
