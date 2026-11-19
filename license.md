# Privacy Policy for Insomnia

**Last Updated:** November 19, 2026

This Privacy Policy explains how the **Insomnia** bot ("the Bot") handles data when installed and used in a Root community.

## 1. Information We Process
Insomnia only processes information when a user explicitly triggers a bot command (such as `/tr <language> <text>`):
- **Message Content:** The text included after the `/tr` command and target language code.
- **Basic Context:** Your community member nickname, user ID, and the channel ID required to post the translated reply back into the channel.

Regular channel messages that do not start with the Bot's command prefix are ignored and are never logged or sent outside of Root.

## 2. Data Storage and Retention
- **No Persistent Storage:** Insomnia does not use a database and does not store message contents, translation history, or user profiles.
- **Transient Processing:** Command text is processed strictly in memory for the duration of the translation request and is immediately discarded once the reply is sent.

## 3. Third-Party Services
To generate translations, the text provided in a `/tr` command is transmitted over an encrypted HTTPS connection to a third-party translation API (Google Translate). Only the text to translate and the target language code are transmitted—your Root nickname, user ID, and community ID are not sent to the translation provider.

## 4. Data Sharing
We do not sell, rent, trade, or share any user or community data with third parties for advertising, profiling, or analytics.

## 5. Control and Removal
Community administrators can stop all data processing at any time by removing Insomnia from their community under **Community Settings > Apps**.

## 6. Changes and Contact
We may update this Privacy Policy as new features are added to the Bot. If you have questions or concerns, please open an issue on our [GitHub Repository](https://github.com/YOUR_USERNAME/YOUR_REPO) or contact the developer at `YOUR_EMAIL_OR_ROOT_HANDLE`.
