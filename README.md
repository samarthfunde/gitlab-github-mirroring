# GitLab to GitHub Repository Mirroring

This repository is automatically mirrored from GitLab to GitHub using GitLab's repository mirroring feature.

## 📋 Overview

This project demonstrates automatic repository synchronization between GitLab and GitHub. Any changes pushed to the GitLab repository are automatically reflected in this GitHub repository.

## 🔄 How It Works

The mirroring is set up using GitLab's push mirroring feature:

1. **Source Repository**: GitLab - `replicate-repo`
2. **Mirror Repository**: GitHub - `gitlab-github-mirroring`
3. **Sync Method**: Push (GitLab → GitHub)

Whenever code is committed to the GitLab repository, it automatically syncs to this GitHub repository.

## ⚙️ Setup Steps

### Prerequisites
- GitLab account with a repository
- GitHub account with a repository
- GitHub Personal Access Token with `repo` permissions

### Configuration Steps

1. **Create repositories**:
   - GitLab: Create project named `replicate-repo`
   - GitHub: Create repository named `gitlab-github-mirroring`

2. **Generate GitHub Token**:
   - Go to GitHub Settings → Developer settings → Personal access tokens
   - Generate new token with `repo` scope
   - Copy the token securely

3. **Configure GitLab Mirroring**:
   - Navigate to your GitLab project
   - Go to **Settings** → **Repository** → **Mirroring repositories**
   - Add the following details:
     - **Git repository URL**: `https://github.com/YOUR_USERNAME/gitlab-github-mirroring.git`
     - **Mirror direction**: Push
     - **Authentication method**: Username and password
     - **Username**: Your GitHub username
     - **Password**: Your GitHub personal access token
   - Click **Mirror repository**

4. **Verify Setup**:
   - Create a test file in GitLab
   - Check if it appears automatically in the GitHub repository

## 🚀 Usage

Simply work on your GitLab repository as usual. All changes will be automatically pushed to GitHub within a few minutes.

## 📝 Notes

- Mirroring is **one-way** (GitLab → GitHub)
- Changes made directly on GitHub will **not** sync back to GitLab
- Sync typically happens within 5 minutes of pushing to GitLab
- You can manually trigger a sync from GitLab's mirroring settings

## 🔐 Security

- Never commit your GitHub token to the repository
- Store tokens securely and rotate them periodically
- Use tokens with minimum required permissions

Happy Learning!
