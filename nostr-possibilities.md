# Nostr Possibilities

Nostr could be so much more than social media. The purpose of this document is to store and explain the various ideas I've come up with for those non-social-media use-cases for Nostr.

## Websites on Nostr

These websites would be similar to ordinary website, except with better privacy and better resilience. All communication would take place via Nostr relays, and the communication would be end-to-end encrypted. Nostr websites would be posted across many relays, and hyperlinks to each websites would contain the URLs for those relays. These websites would be real websites, just as interactive as ordinary websites, not static Markup documents.

## Person-to-Person Communication

### Encrypted Chat

Take something like Signal or SimpleX Chat and re-build it to use Nostr relays. 

### Email Replacement

Email is a truly aweful protocol, especially because it is centralized and it has no resistance to spam. For crying out loud, email is the primary means of deliverying ransomware and phishing. This email replacement would have some similarities with SimpleX Chat.

## Machine-to-Machine Communication

### Command-and-Control

Each end-point in the network would listen to one or more Nostr relays. The central server would issue a command to an end-point via one of the relays that the end-point is listening to. The end-point would respond with the result of copmpleting the command (e.g. error, success, etc); it would send the result to the central command via a Nostr relay that the central command listens on. Each communication would occur on a randomly selected relay.

## Human-to-Machine Communication

### SSH

There are two possibilities for this:
- The SSH server and SSh client would use Nostr to negotiate a pwnat connection. This owuld only work if the routers that the server and client are behind doesn't specifically block pwnat connection.
- The server and client could communicate via a Nostr relays, using ephemeral Nostr events.

It would be appropriate to modify Mosh to communicate via Nostr relays and to understand that SSH sessions could be established redundantly across multiple Nostr relays.
