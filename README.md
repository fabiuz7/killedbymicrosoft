<div align="center">
  <img src="src/assets/tombstone.png" alt="tombstone" style="height: 80px; width: 80px; padding: 0 20px;">
  <h1>Killed by Microsoft</h1>
  <p>A tribute and log of beloved products and services killed by Microsoft.</p>
</div>

<div align="center">

[![MIT license](https://img.shields.io/badge/License-MIT-blue.svg)](/LICENSE) 



</div>

## Contribute

To add a product, gather the following information:

- Name of Product (`name`) - the name of the product
- Launch Date (`dateOpen`) - it should be the date of first release or at least the "beta" or when it is made avaialbe to the customer, do not confuse with the product's announcement
- Discontinued Date (`dateClose`) - it should be the date when the product is "no longer available for purchase" or, for web-based services, when the service stops its normal functioning
- Description (`description`) - a bried description of the product
- Link (`link`) - Relevant link to the source
- Links (`links`) - other relevant links to the source, since all the information may not be available at the same link. Actually this field is not rendered
- Type (`type`) - one of app, service or hardware


### Description
The description should be a single sentence describing the product. It should begin with the products name. For example, "Google Reader was an RSS/Atom feed aggregator." It will be attached to a generated sentence like "Killed about 5 years ago, Google Reader was an RSS/Atom feed aggregator."

Please be respectful, only use past tense.

### Link
Link should be a resource that mentions the discontinuation date and talks about the product. Wikipedia is perfect.

### Type
The type should be either `app`, `service`, or `hardware` as a string.

If you are not familiar with or do not want to use `git`, submit a [new issue](https://github.com/fabiuz/killedbymicrosoft/issues/new?template=add-an-obituary.md) requesting the change. If you are already familiar with `git`, follow these steps:

1. If you haven't already, start by [forking](https://help.github.com/en/articles/fork-a-repo) this repository. 
2. [Create a new branch](https://help.github.com/en/desktop/contributing-to-projects/creating-a-branch-for-your-work) in your fork. Name it using the product you want to add 
3. Switch to that branch (should happen automatically if you've just created it) and open the `graveyard.json` file
4. Use the information gathered above to add a JSON entry in the following format (note the alphabetical order of keys):
```
  {
    "dateClose": "YYYY-MM-DD",
    "dateOpen": "YYYY-MM-DD",
    "description": "[Product Name] was a single sentence overview of the product or service.",
    "link": "https://any.link-to-a.source/will/work-and-wikipedia-is-cool",
    "links": [
      "https://any.link-to-a.source/will/work-and-wikipedia-is-cool"
    ]
    "name": "[Product Name]",
    "type": "app|service|hardware"
  }
```
5. Finally, [create a Pull Request (PR)](https://help.github.com/en/articles/creating-a-pull-request) using the newly created branch (Important: DON'T use the `master` branch for the PR). Submit it with the necessary explanations.  

For code contributions outside of `graveyard.json`, check out the [Contributing Guide](.github/CONTRIBUTING.md).


## Install and build

    yarn install
    node bin/graveyard
    yarn dev

The script in bin/graveyard.js updates graveyard.json and copy it in proper directory. 
Jest is used to test the project and in particular to test the format of graveyard.json. To run it type:

    yarn jest

Then, to create the production version:

    yarn build

## Thanks Where Thanks is Due
I'd like to thank the [Wikimedia Foundation](https://wikimediafoundation.org) and [Internet Archive](https://archive.org/) for their wonderful resources, including the ability to track down broken links, home page graphics, and screenshots of services from the past. They have been invaluable tools in gathering information and content for Killed by Microsoft. If you are able, I encourage you to make a donation to these organizations for the wonderful work they do in sharing knowledge and preserving history.
