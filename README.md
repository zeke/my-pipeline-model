# ziki's pipeline model

An example cog model that internally uses the [Replicate Python SDK](https://github.com/replicate/replicate-python) to generate an image based on the input prompt.

This uses two models hosted on Replicate:

 - [anthropic/claude-3.5-haiku](https://replicate.com/anthropic/claude-3.5-haiku) - to generate the prompt.
 - [black-forest-labs/flux-schnell](https://replicate.com/black-forest-labs/flux-schnell)

It requires a Replicate API token available on your path:

    export REPLICATE_API_TOKEN=<your token here>

Then the model can be run locally using:

    cog predict --use-replicate-token --x-pipeline -i prompt="a toy panda eating ice cream"

This will output the result to output.webp.

## Local development

Start Docker (or Orbstack) and run:

    script/test

## Deployment

Push your model to Replicate with the `--x-pipeline` flag:

    cog push --x-pipeline r8.im/<username>/<model>
