
## Cookbook: Basic Security Protection

Description: Cookbook which can be used as a starting point for security

_This cookbook contains a set of low effort recipes that can be used to detect, fix and prevent common recurring critical and high severity vulnerabilities. Enabling this cookbook will set a security baseline. The expected outcome from this cookbook is not to fix issues that are currently present in the codebase. Because we expect that these flaws have been detected by existing security measures such as peer reviews, penetration tests, and SAST tools. The main purpose is that we prevent new instances of these issues from being introduced in the codebase. Because catching these typical flaws late during development or even in production would increase the cost and time of fixing the issues significantly. Overall, this cookbook gives you the opportunity to improve the state of security by preventing the reappearance from common flaws._

## Injection

Injection flaws occur when an attacker can send hostile data to an interpreter. This interpreter could be used to read or execute SQL, LDAP, XPath, NoSQL, Code, OS commands, XML documents, etc.

### APIs that will be protected by these recipes

Code Injection:

- org.yaml.snakeyaml.Yaml

LDAP injection:

- javax.naming.directory.DirContext

SQL injection:

- java.sql.Statement
- java.sql.Connection

XML Injection:

- javax.xml.parsers.DocumentBuilderFactory
- javax.xml.parsers.SAXParserFactory
- javax.xml.transform.TransformerFactory
- javax.xml.validation.SchemaFactory
- javax.xml.xpath.XPathFactory

## XML External Entities

An XML External Entity attack is a type of attack against an application that parses XML input. This attack occurs when XML input containing a reference to an external entity is processed by a weakly configured XML parser. This attack may lead to the disclosure of confidential data, denial of service, server side request forgery, port scanning from the perspective of the machine where the parser is located, and other system impacts.

### APIs that will be protected by these recipes

- javax.xml.parsers.DocumentBuilderFactory
- javax.xml.stream.XMLInputFactory


## Weak Cryptography

Correctly implementing cryptography can be challenging. Not only is a cryptographic strong algorithm required, the key generation and storage process are also important. Failing in implementing one of these areas correctly could give the attacker the possibility to derive plaintext information from a - what is supposed to be - encrypted message.

### APIs that will be protected by these recipes

- java.security.KeyFactory
- javax.crypto.Cipher
- javax.crypto.KeyAgreement
- javax.crypto.KeyGenerator
- javax.crypto.KeyPairGenerator
- javax.crypto.NullCipher
- javax.crypto.SecretKeyFactory
- javax.crypto.Signature
- javax.net.ssl.SSLContext

## Incorrect controls

Incorrectly implementing security controls could allow hackers to bypass these mechanisms and yield their presence ineffective.

### APIs that will be protected by these recipes

Input validation

- java.lang.String
