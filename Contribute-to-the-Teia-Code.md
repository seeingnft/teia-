# How to Contribute to Teias Code

We're trying to optimize the source code little by little, and it is only fair to write some notes on the thinking behind why we're making some of the decisions we're making. Writing this down will help you (the contributor) get comfortable with the source code.

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

## PR

Pull requests should be as small as possible. At the moment there are a lot of eslint errors everywhere, and instead of fixing them all in one go (potentially breaking something and not being able to identify exactly what broke it), we're deciding to go page by page, component by component, fixing those warnings, removing unused code, etc.

Because it's been a very small team contributing to this project, we've been mainly contributing directly into the `main` branch, but that won't happen anymore.

We will be using a Git flow approach. This means that you will need to create a feature branch from the `develop` branch, write all your code there, and then when you submit your PR you submit it against the `develop` branch. Once the features on `develop` are tested and ready to push to production, an Admin will create a PR from `develop` to `main` and kick off a deployment.

If Git flow is something new to you, don't feel intimidated, come and join us on Discord and we'll take the time to help.


