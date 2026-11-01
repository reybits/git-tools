# Git Helpers

A collection of Git-related helper functions for streamlining your workflow. These helpers are designed to simplify common Git tasks and improve your productivity.

## DISCLAIMER

This script is provided "as is", without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose, and noninfringement. In no event shall the author be liable for any claim, damages, or other liability, whether in an action of contract, tort, or otherwise, arising from, out of, or in connection with the script or the use of this script.

## Installation

Clone the repository and add it to your `PATH`:

```sh
git clone https://github.com/reybits/git-tools.git ~/.git-tools
```

Then, add the following to your `.bashrc`, `.zshrc`, or appropriate shell configuration file:

```sh
export PATH=~/.git-tools:$PATH
```

## Usage

Here’s a list of available Git helpers:

- **gitsr**: Safely remove a git submodule (deinit, cleanup, auto-commit). Usage: `gitsr <submodule_path>`
- **gitupmod**: Update all submodules to the latest commit. Optionally switches to a specified branch first. Usage: `gitupmod [branch]`
- **gitstatmod**: Show a compact status of all submodules, listing only those with working-tree changes or unpushed commits. Usage: `gitstatmod`

*For more information on each helper function, check the individual documentation in the helper files.*

## Versioning

Each script is versioned on its own: the version is the `# Version: X.Y.Z` line in the script header. A version change is a separate commit, `chore(version): bump <script> to X.Y.Z`, that touches nothing else. The increment follows the commits since the previous bump: `feat` raises minor; `fix`, `refactor`, `perf`, `build` and `chore` raise patch; a breaking change (`!`) raises major.

Releases are not tagged: the scripts are used straight from a clone, and the bump commit already marks each version. A script's version history:

```sh
git log --oneline -G'^# Version:' -- gitupmod
```

## Customization

You can modify these helpers to add more functionality or adjust them according to your Git workflow. Simply edit the respective helper functions within the source files.

## Contributing

Feel free to fork this repository and create pull requests. Any improvements or bug fixes are welcome!

## License

This project is licensed under the MIT License - see the `LICENSE` file for details.
