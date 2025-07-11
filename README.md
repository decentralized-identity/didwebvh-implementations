# didwebvh-implementations

This is a repository of existing DID WebVH implementations used for interoperability and conformance testing.

## Adding a new implementation

### Self-Hosted

Submit a PR adding your DID to the `implementations/registry.json` file.
```json
{
    "registry": {
        ...
        "did:webvh:{SCID}:example.com:my-implementation": {
            "name": "My Implementation",
            "url": "https://example.com"
        }
    }
}
```

### GH Hosted

#### Create your DID
Use the `https://identity.foundation/didwebvh-implementations/implementations/{name}` origin.

Ex: `did:webvh:{SCID}:identity.foundation:didwebvh-implementations:implementations:my-implementation`

#### Submit a PR
Fork the repo, then create your implementation's directory. For example, if your implementation's name is `my-implementation`, create a directory called `my-implementation` in the implementations directory and include any relevent files (`did.jsonl`, `did-witness.json`, `did.json`, `whois.vp`, etc...).

Your DID will be hosted through a gh page upon merging.

You will also need to edit the `implementations/registry.json` file to add your DID. For GH Hosted DIDs, you need to add the `directory` property to your submission.
```json
{
    "registry": {
        ...
        "did:webvh:{SCID}:identity.foundation:didwebvh-implementations:implementations:my-implementation": {
            "name": "My Implementation",
            "url": "https://example.com",
            "directory": "my-implementation"
        }
    }
}
```

## Updating an existing implementation

To update your existing implementation, open a PR in which you update relevent documents from your implementation's directory if needed and edit the SCID/DID value from the `implementations/registry.json` file if needed.

## Testing your implementation before submitting a PR

TBD