# ziki's pipeline model

This is simple Cog model to test using the Stainless implementation of Replicate's Python SDK, with support for `use()` and fetching API token from Cog's current scope, as an alternative to using REPLICATE_API_TOKEN from the environment.

## Usage

```
git clone https://github.com/zeke/my-pipeline-model
cd my-pipeline-model

script/build
script/build
```

Note you might need to go digging for a generated requirements.txt file in the .cog directory, and set `replicate==2.0.0a22` manually for this to work.