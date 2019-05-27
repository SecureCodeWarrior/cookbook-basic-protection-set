
#### API's that have been researched but don't have the ability to be exploited

- Google GSON: requires root type, honors property types and polymorphism isn't enabled by default
- minimal-JSON: parses to a map
- json.org: parses to JSONObjects that can't execute code
- toml4j
- ini4j

#### API's that have been researched but cannot be fixed with a default fix

- java.lang.Runtime#exec: the fix is opinionated, the suggested way to prevent os command injections and secure this API is by using a custom input sanitazation / validation routine
- jYaml: parser has no mechanism for type whitelisting or blacklisting
- YamlBeans: parser has no mechanism for type whitelisting or blacklisting
- Jackson ObjectMapper#enableDefaultTyping: this has to be explicitly configured so we should suppose they know what the drawbacks are
