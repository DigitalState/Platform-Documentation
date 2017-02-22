# Subtrees

## Creating a Subtree Bundle

Below are the steps required to create a subtree bundle. In this example, the subtree bundle will reside in `src/Ds/Bundle` and will be named `DefinitionBundle`.

- Create a repository named `Platform-Definition-Bundle` on GitHub.
- Integrate the repository with Packagist on GitHub (Settings / Integrations & services / Add service / Packagist).
- Create a new project for the repository.
- Clone the repository inside your project root `git clone git@github.com:DigitalState/Platform-Definition-Bundle.git .`.
- Create develop branch locally `git checkout -b develop`.
- Push develop branch `git push origin develop`.
- Set develop branch as default on GitHub (Settings / Branches / Default branch)
- Add a remote repository to the parent repository `git remote add -f platform-definition-bundle git@github.com:DigitalState/Platform-Definition-Bundle.git`.
- Add the subtree using remote shortcut `git subtree add --prefix src/Ds/Bundle/DefinitionBundle platform-definition-bundle develop --squash`.
- Add necessary code in your bundle.
- Commit your code from parent repository.
- Push subtree to its repository `git subtree push --prefix=src/Ds/Bundle/DefinitionBundle platform-definition-bundle develop`.
