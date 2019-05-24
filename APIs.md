
#### API's that have been researched but don't have the ability to be exploited

#### API's that have been researched but cannot be fixed with a default fix

- java.lang.Runtime#exec: the fix is opinionated, the suggested way to prevent os command injections and secure this API is by using a custom input sanitazation / validation routine
