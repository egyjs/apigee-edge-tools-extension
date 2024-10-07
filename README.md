# Apigee Edge Proxy Revision Diff Tool

## Overview

This TypeScript module provides a comprehensive solution for fetching, downloading, and comparing different revisions of Apigee Edge proxies. It includes functions to retrieve proxy revisions, download revision bundles, and display a diff viewer for comparing two revisions.

## Features

- **Fetch Proxy Revisions**: Retrieve a list of revisions for a specific proxy within an organization.
- **Download Revision Bundles**: Download the bundle for a specific revision of a proxy.
- **Revision Selector**: Dynamically create and insert a revision selector into the DOM.
- **Diff Viewer**: Open a new window to display a side-by-side comparison of two proxy revisions using JSZip and jsdiff libraries.

## Dirct Use
download the ZIP file of the ext: https://github.com/egyjs/apigee-edge-tools-extension/releases/download/1.1/chrome.zip
and use it in: 
`chrome://extensions/`

## Functions

- [`delay(ms: number)`](command:_github.copilot.openSymbolFromReferences?%5B%22%22%2C%5B%7B%22uri%22%3A%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2Fc%3A%2FUsers%2Fel3za%2Fwork%2Fapigee-edge-tools-extension%2Fsource%2FTools%2Fapigee-edge.ts%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%2C%22pos%22%3A%7B%22line%22%3A1%2C%22character%22%3A6%7D%7D%5D%2C%226f3e537e-5db1-4dcd-92b4-a445e674e039%22%5D "Go to definition"): Introduces a delay in milliseconds.
- [`getProxyRevisions(org: string, proxy: string)`](command:_github.copilot.openSymbolFromReferences?%5B%22%22%2C%5B%7B%22uri%22%3A%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2Fc%3A%2FUsers%2Fel3za%2Fwork%2Fapigee-edge-tools-extension%2Fsource%2FTools%2Fapigee-edge.ts%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%2C%22pos%22%3A%7B%22line%22%3A3%2C%22character%22%3A6%7D%7D%5D%2C%226f3e537e-5db1-4dcd-92b4-a445e674e039%22%5D "Go to definition"): Fetches the list of revisions for a given proxy.
- [`downloadRevisionBundle(org: string, proxy: string, revision: string)`](command:_github.copilot.openSymbolFromReferences?%5B%22%22%2C%5B%7B%22uri%22%3A%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2Fc%3A%2FUsers%2Fel3za%2Fwork%2Fapigee-edge-tools-extension%2Fsource%2FTools%2Fapigee-edge.ts%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%2C%22pos%22%3A%7B%22line%22%3A18%2C%22character%22%3A6%7D%7D%5D%2C%226f3e537e-5db1-4dcd-92b4-a445e674e039%22%5D "Go to definition"): Downloads the bundle for a specific revision.
- [`createRevisionSelectorTemplate(currentRev: string, revisions: string[])`](command:_github.copilot.openSymbolFromReferences?%5B%22%22%2C%5B%7B%22uri%22%3A%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2Fc%3A%2FUsers%2Fel3za%2Fwork%2Fapigee-edge-tools-extension%2Fsource%2FTools%2Fapigee-edge.ts%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%2C%22pos%22%3A%7B%22line%22%3A27%2C%22character%22%3A6%7D%7D%5D%2C%226f3e537e-5db1-4dcd-92b4-a445e674e039%22%5D "Go to definition"): Creates an HTML template for the revision selector.
- [`insertRevisionSelector(template: string)`](command:_github.copilot.openSymbolFromReferences?%5B%22%22%2C%5B%7B%22uri%22%3A%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2Fc%3A%2FUsers%2Fel3za%2Fwork%2Fapigee-edge-tools-extension%2Fsource%2FTools%2Fapigee-edge.ts%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%2C%22pos%22%3A%7B%22line%22%3A44%2C%22character%22%3A6%7D%7D%5D%2C%226f3e537e-5db1-4dcd-92b4-a445e674e039%22%5D "Go to definition"): Inserts the revision selector into the DOM.
- [`diff()`](command:_github.copilot.openSymbolFromReferences?%5B%22%22%2C%5B%7B%22uri%22%3A%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2Fc%3A%2FUsers%2Fel3za%2Fwork%2Fapigee-edge-tools-extension%2Fsource%2FTools%2Fapigee-edge.ts%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%2C%22pos%22%3A%7B%22line%22%3A55%2C%22character%22%3A6%7D%7D%5D%2C%226f3e537e-5db1-4dcd-92b4-a445e674e039%22%5D "Go to definition"): Main function to initiate the diff process, fetch revisions, download bundles, and set up the diff viewer.
- [`openDiffUI(rev1: { rev: string, bundle: Blob }, rev2: { rev: string, bundle: Blob })`](command:_github.copilot.openSymbolFromReferences?%5B%22%22%2C%5B%7B%22uri%22%3A%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2Fc%3A%2FUsers%2Fel3za%2Fwork%2Fapigee-edge-tools-extension%2Fsource%2FTools%2Fapigee-edge.ts%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%2C%22pos%22%3A%7B%22line%22%3A86%2C%22character%22%3A12%7D%7D%5D%2C%226f3e537e-5db1-4dcd-92b4-a445e674e039%22%5D "Go to definition"): Opens a new window to display the diff UI for comparing two revisions.

## Usage

1. **Fetch Revisions**: Call [`getProxyRevisions`](command:_github.copilot.openSymbolFromReferences?%5B%22%22%2C%5B%7B%22uri%22%3A%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2Fc%3A%2FUsers%2Fel3za%2Fwork%2Fapigee-edge-tools-extension%2Fsource%2FTools%2Fapigee-edge.ts%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%2C%22pos%22%3A%7B%22line%22%3A3%2C%22character%22%3A6%7D%7D%5D%2C%226f3e537e-5db1-4dcd-92b4-a445e674e039%22%5D "Go to definition") with the organization and proxy name to get the list of revisions.
2. **Download Bundles**: Use [`downloadRevisionBundle`](command:_github.copilot.openSymbolFromReferences?%5B%22%22%2C%5B%7B%22uri%22%3A%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2Fc%3A%2FUsers%2Fel3za%2Fwork%2Fapigee-edge-tools-extension%2Fsource%2FTools%2Fapigee-edge.ts%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%2C%22pos%22%3A%7B%22line%22%3A18%2C%22character%22%3A6%7D%7D%5D%2C%226f3e537e-5db1-4dcd-92b4-a445e674e039%22%5D "Go to definition") to download the bundles for the current and selected revisions.
3. **Display Diff**: Call [`diff`](command:_github.copilot.openSymbolFromReferences?%5B%22%22%2C%5B%7B%22uri%22%3A%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2Fc%3A%2FUsers%2Fel3za%2Fwork%2Fapigee-edge-tools-extension%2Fsource%2FTools%2Fapigee-edge.ts%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%2C%22pos%22%3A%7B%22line%22%3A55%2C%22character%22%3A6%7D%7D%5D%2C%226f3e537e-5db1-4dcd-92b4-a445e674e039%22%5D "Go to definition") to initiate the process and display the diff viewer.

## Dependencies

- **JSZip**: For handling ZIP file operations.
- **jsdiff**: For generating the diff between two text files.

## Example

```typescript
import { diff } from './apigee-edge';

// Call the diff function to start the process
diff();
```

## License

This project is licensed under the MIT License. See the LICENSE file for details.

---

Optimize your Apigee Edge proxy management with this powerful revision diff tool. Easily fetch, download, and compare proxy revisions to streamline your development and debugging process.
