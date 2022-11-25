# network.txt

A proposed standard for giving information about 3rd party data transmission.

Readable by humans AND programs alike.

## Background

There are many txt file standards out there like [robots.txt](http://www.robotstxt.org), [security.txt](https://securitytxt.org) or [humans.txt](https://humanstxt.org).

While robots.txt offers a useful standard for programs, most other .txt files are intended for humans to read.

Since the GDPR laws were passed in Europe and many countries outside of the EU also have similar intents, a standard for providing information about shared data should be useful for (1) visitors of websites to know, where the data gets shared and (2) for developers who create new tools which allow easier handling of GDPR.

## File Format

The network.txt describes what 3rd party providers are used and where you can find the privacy policy as well as the terms of the website.

The providers which can't be disabled should come first and optional providers later.

Example:

```
# LINKS

Policy: http://www.example.org/Policies/Privacy
Terms: http://www.example.org/Terms

# THIRD PARTY PROVIDERS

Name: Cloudflare
URL: https://www.cloudflare.com
Use: Necessary
For: DDoS protection

Name: Google Analytics
URL: https://analytics.google.com
Use: Optional
For: Analytics
```

## Other projects

Some other developers also thought about this Issue:

* [P3P](https://www.w3.org/P3P/) The Platform for Privacy Preferences Project (P3P) is an obsolete protocol allowing websites to declare their intended use of information they collect about web browser users. 
* [privacy.txt](https://github.com/jasonlotito/privacytxt) Would offer a standard to easily find privacy policies and TOS. It never got popular.

## History

After reading [this comment](https://news.ycombinator.com/item?id=33740717) on a HN discussion about humans.txt I came to the conclusion that such a file would be way more useful than humans.txt and began writing this standard.
