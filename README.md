# Gatsby Json Crasher

Repro project for gatsby develop crashing when a json file is in a directory starting with a numeric character.

Clone it.. 
```sh
npm i
gatsby develop
```
booom....

When running gatsby develop if you have the gatsby-transformer-json installed and anywhere in you file system you have a .json file directly inside a directory that starts with a number gatsby will crash with (this folder was called 20m

```
⠋ building schema
 ERROR
UNHANDLED REJECTION Syntax Error: Unexpected Int "20"
  GraphQLError: Syntax Error: Unexpected Int "20"
  - TypeMapper.js:113 TypeMapper.createType
    [gatsby-json-crasher]/[graphql-compose]/lib/TypeMapper.js:113:43
  - ObjectTypeComposer.js:80 Function.createTemp
  - ObjectTypeComposer.js:56 Function.create
    [gatsby-json-crasher]/[graphql-compose]/lib/ObjectTypeComposer.js:56:21
  - index.js:59
    [gatsby-json-crasher]/[gatsby]/dist/schema/infer/index.js:59:41
  - Array.forEach
  - index.js:42 addInferredTypes
    [gatsby-json-crasher]/[gatsby]/dist/schema/infer/index.js:42:13
  - schema.js:95 async buildSchema
    [gatsby-json-crasher]/[gatsby]/dist/schema/schema.js:95:3
  - index.js:136 async Object.build
    [gatsby-json-crasher]/[gatsby]/dist/schema/index.js:136:18
  - index.js:412 async module.exports
    [gatsby-json-crasher]/[gatsby]/dist/bootstrap/index.js:412:3
```
