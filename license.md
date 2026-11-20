# Privacy Policy for Insomnia

**Last Updated:** November 19, 2026

This Privacy Policy explains how the **Insomnia** bot ("the Bot") collects, processes, and stores data when installed and used in a Root community.

## 1. Information We Process
Insomnia processes message and context data in the following scenarios:
- **Direct Commands:** When a user invokes `/tr` (including `/tr setup`, `/tr last`, `/tr @user`, `/tr auto`, or `/tr <language> <text>`), the Bot reads the command arguments, the sender's user ID, nickname, and the channel ID to execute the request and post the response.
- **Replied-To Messages:** When a user replies to a message with `/tr`, the Bot retrieves the referenced message's text and author nickname from its short-term cache or the Root API in order to translate it.
- **Channel Auto-Translate Mode:** In channels where `/tr auto on` has been explicitly enabled, the Bot processes all incoming text messages in that channel to detect their language and post translations when they differ from the channel's configured target language. In channels where auto-translate is off, non-command messages are never sent to external translation services.

## 2. Data Storage and Retention
- **Short-Term In-Memory Message Cache:** To support reply and recent-history translations (`/tr`, `/tr last`, `/tr @user`), Insomnia temporarily holds a rolling buffer of recent channel messages in memory (up to 50 messages per channel and 500 messages globally). These messages are never written to a database and are automatically overwritten as new messages arrive or cleared when the Bot restarts.
- **Persistent Configuration Preferences:** To remember user and channel settings across restarts, Insomnia stores minimal configuration files containing:
  - **User Language Preferences:** Your Root User ID paired with your chosen target language code (set via `/tr setup`).
  - **Channel Auto-Translate Settings:** The Root Channel ID paired with the channel's target language code (set via `/tr auto on`).

## 3. Third-Party Services
To generate translations, message text and the target language code are transmitted over an encrypted HTTPS connection to Google Translate. Your Root nickname, User ID, and Channel ID are never included in requests sent to the translation provider.

## 4. Data Sharing
We do not sell, rent, trade, or share any user messages, identifiers, or community data with third parties for advertising, profiling, or analytics.

## 5. Control and Data Removal
- **Disable Channel Auto-Translate:** Run `/tr auto off` in any channel at any time to stop automatic translation of incoming messages.
- **Update Language Preferences:** Run `/tr setup <language>` at any time to overwrite your saved target language.
- **Full Removal:** Community administrators can stop all data processing at any time by removing Insomnia under **Community Settings > Apps**.

## 6. Changes and Contact
We may update this Privacy Policy as new features are added to the Bot. If you have questions or would like your stored user ID preference deleted, please open an issue on our [GitHub Repository](https://github.com/YOUR_USERNAME/YOUR_REPO).
