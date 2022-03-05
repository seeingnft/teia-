# How to Contribute to Teias Code

You can contribute to Teia in the following ways: 
* Fix bugs
* Code development
* Maintain documents
* Translate documents

You will need to have basic Git skills and have a GitHub account.

Here are the steps to contribute:
- Create a fork of [https://github.com/teia-community/teia-ui](https://github.com/teia-community/teia-ui)
- Create a feature/fix branch on the fork using the following fork naming convention: `<feature-or-fix>/<feature-name-or-issue-id>`
- Implement the feature/fix
- Create a pull request to teia-ui
- Verify the [automated build](https://github.com/teia-community/teia-ui/actions) succeeded
- Request a code review

If all goes well, your pull request is merged. Keep your pull request as small as possible so it's easier to add it to the main repository. For questions, reach the dev team in the #general-dev channel of the [Teia Discord](https://discord.gg/QckkbVMcWu). 

Thanks for your willingness to help with this project.

## Learning Resources
[OBJKT NFTs](https://leonnicholls.medium.com/hic-et-nunc-nfts-61743765b2ac?source=user_profile---------6----------------------------)

[Hicdex: the Hic Et Nunc indexer](https://leonnicholls.medium.com/hicdex-the-hic-et-nunc-indexer-bd45f27a228f)

[OBJKT Metadata](https://leonnicholls.medium.com/hic-et-nunc-metadata-40e594530e31)

[Minters for Hic Et Nunc](https://leonnicholls.medium.com/minters-for-hic-et-nunc-8b244b3d7ce0?source=user_profile---------1----------------------------)

[Hic Et Nunc Smart Contracts (Part 1)](https://leonnicholls.medium.com/hic-et-nunc-smart-contracts-part-1-e4ad5d0934b9)

## PR

We take PRs on a case-by-case basis. Please contact us in the discord in the #general-dev channel to have your PR considered.

You will need to create a feature branch from the `main` branch, write all your code there, and then when you submit your PR you submit it against the `main` branch.

If anything else is new to you, don't feel intimidated, come and join us on [Discord](https://discord.gg/AQ56zrn55w) and we'll take the time to help.

## Components

When creating a component you need to provide a few properties in order to render the component properly. Try to avoid creating prop drilling, or even accessing react context in a component. The components should be as dumb as possible. The only place where you should have access to API requests, or React.Context is at the page level (`src/pages/*`).

In terms of standard its a good practice to first do global imports, then relative imports and finally scss imports. So a component would look something like this:

```jsx
import React from 'react' // a global import
import { Button } from '../button' // a relative import
import styles from './styles.module.scss' // a sass import

export const MyComponent = () => {
  return <div className={styles.container}>My Component</div>
}
```

There are some auxiliary components that aren't doing much besides aiding with the layout. A good example of that is the `/src/pages/objkt-display` where you have `<Container/>` and `<Padding />`. These components are similar to what `reactstrap` provides, but we're trying to minimize our bundle size, so we're reducing on dependencies.

