# ![ForkDelta logo](https://forkdelta.github.io/next/favicon-32x32.png) ForkDelta Tokenbase

[![Build Status](https://travis-ci.org/forkdelta/tokenbase.svg?branch=master)](https://travis-ci.org/forkdelta/tokenbase) [![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](https://github.com/forkdelta/tokenbase/issues)

**ForkDelta** is a decentralized exchange with over 700 tradable ERC20-compliant tokens. Tokenbase is our ERC20 token knowledgebase.

## Format
Token information is stored in YAML format, one token per file, in `tokens/0xTOKENADDRESS.yaml`.

### Common YAML
* ` # Comment` is a YAML comment. The hash `#` must be preceded by a space.
* `key: value` is a key-value pair.
* `- item` is a list entry. It is possible to have a list entry of a non-scalar type, e.g.: `- key: value` is a list entry containing a key-value pair.

### Required
A token listing file must include the following information:

```yaml
---  # Mandatory "start of the document" marker
addr: '0x…'  # token contract address, in single quotes
decimals: 18 # Token decimals
name: Human Readable Token Name  # Required
symbol: TOKEN  # Required: Token symbol
```

### Description
Description of the token can be included:

```yaml
---
addr: '0xad5fe5b0b8ec8ff4565204990e4405b2da117d8e'
decimals: 0
description: TRXC is an ERC20 token that serves as a social digital currency with all major social network to make the process of sending and receiving money rewarding for everyone.
name: tronclassic
symbol: TRXC
````

If you need more than one line of description, use the folded scalar notation:
```yaml
---
addr: '0xad5fe5b0b8ec8ff4565204990e4405b2da117d8e'
decimals: 0
description: >-
  TRXC is an ERC20 token that serves as a social digital currency with all major social network to make the process of sending and receiving money rewarding for everyone.
 name: Tronclassic
symbol: TRXC
````
Note that folded scalar notation requires two new lines for a paragraph break (like Reddit format).

Description may contain HTML.

### Links
Links can be included to refer the user to external resources relevant to the token. They are represented by a list of key-value pairs, where key is the type of the link. The following types are currently recognized: 
- Bitcointalk https://bitcointalk.org/index.php?topic=3829331
- Blog 
- CoinMarketCap
- Discord
- Email tronclassic.trxc@gmail.com
- Facebook https://www.facebook.com/groups/1853017211395204/
- Github https://github.com/TronClassic-TRXC
- Reddit
- Slack
- Telegram https://t.me/ClassicTron
- Twitter https://twitter.com/TronClassic
- WeChat
- Website https://www.tronclassic.xyz/
- Whitepaper https://drive.google.com/file/d/1_DpQVRTQbR8m3Qj4NGA70sjqhP7Qt_5w/view
- YouTube https://www.youtube.com/channel/UCOwp1XMHOiLJ-meqNS4h8HQ

Example:
```yaml
---
addr: '0xad5fe5b0b8ec8ff4565204990e4405b2da117d8e'
decimals: 0
links:
- Email: mailto:tronclassic.trxc@gmail.com
- Telegram: https://t.me/ClassicTron
- Twitter: https://twitter.com/TronClassic
- Website: https://www.tronclassic.xyz/
- Whitepaper: https://drive.google.com/file/d/1_DpQVRTQbR8m3Qj4NGA70sjqhP7Qt_5w/view
name: TRONCLASSIC
symbol: TRXC
```

### Notice
Notice is a special field used to communicate critical information regarding contract or token status. This information should be prominently displayed to the user before any interaction occurs.
Example:
```yaml
---
addr: '0xad5fe5b0b8ec8ff4565204990e4405b2da117d8e'
decimals: 0
name: TRONCLASSIC
notice: >-
  
  
symbol: TRXC
```
Notice may cointain HTML.
