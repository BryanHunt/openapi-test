To reproduce the problem:

- git clone
- yarn install
- yarn build

You should get the following errors:

```
node_modules/openapi3-ts/src/model/oas-common.ts:21:16 - error TS7053: Element implicitly has an 'any' type because expression of type 'string' can't be used to index type 'ISpecificationExtension'.
  No index signature with a parameter of type 'string' was found on type 'ISpecificationExtension'.

21         return obj[extensionName];
                  ~~~~~~~~~~~~~~~~~~

node_modules/openapi3-ts/src/model/oas-common.ts:31:9 - error TS7053: Element implicitly has an 'any' type because expression of type 'string' can't be used to index type 'ISpecificationExtension'.
  No index signature with a parameter of type 'string' was found on type 'ISpecificationExtension'.

31         obj[extensionName] = extension;
           ~~~~~~~~~~~~~~~~~~

node_modules/openapi3-ts/src/model/specification-extension.ts:28:13 - error TS7053: Element implicitly has an 'any' type because expression of type 'string' can't be used to index type 'SpecificationExtension'.
  No index signature with a parameter of type 'string' was found on type 'SpecificationExtension'.

28         if (this[extensionName]) {
               ~~~~~~~~~~~~~~~~~~~

node_modules/openapi3-ts/src/model/specification-extension.ts:29:20 - error TS7053: Element implicitly has an 'any' type because expression of type 'string' can't be used to index type 'SpecificationExtension'.
  No index signature with a parameter of type 'string' was found on type 'SpecificationExtension'.

29             return this[extensionName];
                      ~~~~~~~~~~~~~~~~~~~

node_modules/openapi3-ts/src/model/specification-extension.ts:39:9 - error TS7053: Element implicitly has an 'any' type because expression of type 'string' can't be used to index type 'SpecificationExtension'.
  No index signature with a parameter of type 'string' was found on type 'SpecificationExtension'.

39         this[extensionName] = payload;
           ~~~~~~~~~~~~~~~~~~~


Found 5 errors in 2 files.

Errors  Files
     2  node_modules/openapi3-ts/src/model/oas-common.ts:21
     3  node_modules/openapi3-ts/src/model/specification-extension.ts:28
```