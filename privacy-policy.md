# Privacy Policy

**Last Updated: 11-17-2026**

This Privacy Policy explains how Dazzling ("Dazzling," "the bot," "we," "us") collects, uses, stores, and protects information when you use Dazzling on Discord or interact with its official documentation.

Dazzling is developed and operated by an individual developer known on Discord as **omgkawaiialeix** ("the Developer"). For any question about this Policy, contact us through our official Discord support server: **https://discord.gg/R3AZpftXTm**.

By using Dazzling, you also agree to [Discord's own Privacy Policy](https://discord.com/privacy) and [Terms of Service](https://discord.com/terms), since Dazzling operates entirely within the Discord platform and cannot function without it.

---

## 1. Information We Collect

We only collect the information that is strictly necessary for Dazzling's features to work. We group it into three categories:

### 1.1 Content You Create Directly

When a server administrator uses commands such as `/embed create`, `/embed edit`, `/config`, or `/partner message`, Dazzling stores the content that person types or selects, including:

- The text and settings of custom embeds: title, description, color, author name/icon, footer text/icon, image and thumbnail URLs, field text, button labels and URLs, and the internal name/folder used to organize them.
- Which embed and channel are linked to the Welcome, Boost, Goodbye, or Partner (alliance) features.

This content is written voluntarily by server administrators to configure the bot's behavior. We do not generate, suggest, or alter this content ourselves.

### 1.2 Discord Identifiers

To make the features above work per server and per user, we store Discord's own identifiers ("snowflake" IDs):

- The ID of the Discord server (guild) where a feature is configured.
- The ID of the Discord user who created or owns a saved embed, or who configured a feature.
- The ID of the Discord channel selected for a feature (e.g., where a welcome message or alliance alert should be sent).
- The response language (Spanish or Portuguese) a server has selected via `/language`.

We do **not** store real names, email addresses, phone numbers, or physical addresses. We do not have access to any of that information through Discord's API in the first place.

### 1.3 Information Processed Temporarily (Not Stored)

Some information is read or used for a moment to build a message, and is then discarded — it is never written to our database:

- **Member information at the moment of an event**: when someone joins a server (Welcome), boosts it (Boost), leaves it (Goodbye), or posts an invite link in a configured alliance channel (Partner), we briefly use that person's Discord username, tag, mention, and avatar URL to fill in the placeholders (e.g., `{{user.name}}`) of the message the server administrator designed. This information is used only to render that one message and is immediately discarded afterward.
- **Message content in the designated "Partner" channel only**: if a server administrator sets up a channel using `/partner channel`, Dazzling reads the text of messages posted in **that specific channel only**, solely to detect whether a message contains a Discord server invite link. If no invite link is found, nothing happens. If one is found, Dazzling looks up basic public information about that invite (the invited server's name, icon, and approximate member count, obtained directly from Discord) to build an automatic reply.
  - Dazzling does **not** read, process, or store message content from any other channel, for any other purpose.
  - The text of the message itself, and the invite link it contained, are never saved to our database or written to any log.
- **Webhook delivery**: if a server administrator chooses to send an embed through the Webhook option (to show a custom name and/or avatar instead of the bot's own), Dazzling creates or reuses a Discord webhook in that channel to deliver the message. That webhook is created and managed entirely by Discord; we do not store its ID, token, or any related data in our database.

---

## 2. How We Use Information

We use the information described above exclusively to:

- Operate the features you or your server administrators configure (custom embeds, Welcome/Boost/Goodbye automated messages, and the Partner alliance-link detection).
- Let an embed's owner find, edit, rename, move, transfer, or delete their own saved content.
- Maintain, debug, and improve Dazzling's functionality.

We do not use your information for advertising, profiling, or any purpose unrelated to operating the bot's features.

---

## 3. How We Store Information

All of the data described in Sections 1.1 and 1.2 is stored in a SQLite database on Dazzling's hosting infrastructure. Access to our hosting account is protected by two-factor authentication, and our hosting provider includes DDoS protection. That said, like any online service, we cannot guarantee absolute security of data in storage or in transit.

Our hosting provider's console does not keep a permanent log history by default, and any technical logs that may exist temporarily on the hosting infrastructure do not contain the content of your Discord messages. Our hosting provider may delete logs or backups at its own discretion, particularly if they consume significant storage space.

---

## 4. Data Retention and Deletion

- Data linked to a server is kept for as long as Dazzling remains a member of that server, with no fixed expiration date.
- **Automatic deletion**: if Dazzling is removed from a server (kicked, or the server is deleted), all data associated with that server — every saved embed, Welcome/Boost/Goodbye configuration, and Partner configuration — is **automatically and immediately deleted** from our database. This does not happen if a server merely experiences a temporary Discord outage; Dazzling only deletes data when it has genuinely left a server.
- **Manual deletion**: any user can delete their own saved embeds at any time using `/embed delete`, without needing to remove the bot from the server.
- Message content read in the Partner alliance channel, and webhook data (Section 1.3), are never stored in the first place, so there is nothing to delete.
- **If Dazzling is permanently discontinued**, we will make reasonable efforts to delete all remaining stored data within a reasonable time after the Service shuts down.
- If you would like us to delete specific data and the tools above don't cover your situation, you may reach out through our Discord support server and we will address your request.

---

## 5. Sharing of Information

We do not sell, rent, or share your information with third parties for marketing or any other purpose. Information is only ever exchanged with Discord itself, as is inherently necessary for Dazzling to function as a Discord bot, and is subject to Discord's own Privacy Policy.

---

## 6. Children's Privacy

Dazzling is intended to be used in accordance with Discord's own Terms of Service, which require users to meet Discord's minimum age requirement. We do not knowingly collect information from individuals who do not meet that requirement, and we rely on Discord's own age-related enforcement mechanisms.

---

## 7. Your Rights

Depending on where you live, you may have rights over your personal data, including the right to access, correct, or request deletion of your information. If you are located in Colombia, this includes the rights recognized under **Law 1581 of 2012 ("Habeas Data")** and its regulatory decrees. We honor these rights as described in Section 4 above (self-service deletion via `/embed delete`, or automatic deletion when the bot leaves your server). For any other request, contact us through our Discord support server.

---

## 8. Donations

Dazzling may offer a way to support its development voluntarily through Patreon. Donations are processed entirely by Patreon, and any payment or billing information you provide is handled by Patreon under its own Privacy Policy — we do not receive or store your payment details.

---

## 9. International Use

Dazzling can be used by servers and users around the world. By using Dazzling, you understand that your information may be stored and processed on infrastructure located in a different country than your own, and that this Policy and the Terms of Service are governed by the laws of Colombia (see our Terms of Service).

---

## 10. Where These Documents Are Published

This Privacy Policy and our Terms of Service are published as plain text (Markdown) documents in a public GitHub repository, not as a dedicated website. If you view them on GitHub, your visit is also subject to [GitHub's own Privacy Statement](https://docs.github.com/site-policy/privacy-policies/github-privacy-statement), which is separate from and outside of our control.

---

## 11. Changes to This Policy

We may update this Privacy Policy from time to time, for example to reflect new features or legal requirements. When we do, we will update the "Last Updated" date at the top of this page. Continuing to use Dazzling after changes take effect means you accept the updated Policy.

---

## 12. Contact

If you have any questions about this Privacy Policy or how your information is handled, reach out to **omgkawaiialeix** through our official Discord support server: **https://discord.gg/R3AZpftXTm**.
