# n8n-youtube-news-playlist-updation
An automated n8n workflow that monitors a YouTube playlist and automatically replaces expired live stream recordings with the latest active broadcasts via the YouTube Data API v3

🚀 Quick Start
Follow these steps to get the News Playlist Updation workflow running in your own n8n instance:

**1. Prerequisites**
  Before importing, ensure you have the following:

  a. An n8n instance (Cloud, Desktop, or Self-Hosted).

  b. A Google Cloud Project with the YouTube Data API v3 enabled.

  c. Credentials created in your Google Cloud Console:

  d. API Key (for public search requests).

  e. OAuth 2.0 Client ID & Secret (for playlist management).

**2. Import the Workflow**
  a. Download the News_Playlist_Updation.json file from this repository.

  b. Open your n8n dashboard and create a New Workflow.

  c. Click the three dots (⋮) in the top-right corner and select Import from File.

  d. Select the JSON file you just downloaded.

**3. Configure Credentials**
The nodes will appear on your canvas, but they will show connection errors until you add your credentials:

  a. YouTube Nodes: Click on any YouTube node (e.g., "Get All Channels") and select Create New Credential. Enter your Google OAuth 2.0 Client ID and Secret.

  b. HTTP Request Node: Open the "Updated Live Stream HTTP Request" node. Replace the placeholder YOUR_API_KEY_HERE in the URL with your actual Google API Key.

**4. Set Your Playlist ID**
  a. Open the Get All Channels and Add new live streams nodes.

  b. Replace the playlistId value with the ID of your target YouTube playlist (the string of characters after list= in your playlist URL).

**5. Test & Activate**
  a. Click Execute Workflow to run a manual test.

  b. Once verified, toggle the Active switch to keep it running on the hourly schedule.


💻 n8n demo canvas:
<img width="1920" height="1080" alt="n8n project2" src="https://github.com/user-attachments/assets/6e4a31b0-a0c0-4bb0-8fe6-fdbf1f76a717" />
