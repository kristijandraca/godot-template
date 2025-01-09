# Godot Template Project

This is a Godot project template with CI/CD integration to automate the export and upload of your game to itch.io. The project uses GitHub Actions to build and deploy your game for multiple platforms.

## Features

- Automated builds for Windows, Linux, and Web (HTML5) platforms.
- Continuous integration and deployment using GitHub Actions.
- Automatic upload of builds to itch.io.

## Getting Started

### Prerequisites

- [Godot Engine](https://godotengine.org/download)
- [Git](https://git-scm.com/)
- [itch.io account](https://itch.io/)

### Setup

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/godottemplate.git
    cd godottemplate
    ```

2. Open the project in Godot Engine.

3. Configure your export presets in `project.godot`.

### GitHub Actions CI/CD

This project uses GitHub Actions for CI/CD. The workflow is defined in `.github/workflows/godot-ci.yml`.

#### Environment Variables

- `GODOT_VERSION`: The version of Godot to use for the export.
- `EXPORT_NAME`: The name of the exported game.
- `PROJECT_PATH`: The path to the Godot project.
- `ITCH_USERNAME`: Your itch.io username.
- `ITCH_GAME_ID`: The ID of your game on itch.io.

#### Secrets

- `BUTLER_API_KEY`: Your itch.io Butler API key. Add this to your repository secrets.

### Running the Workflow

The workflow is triggered on every push to the `main` branch. It performs the following steps:

1. Checks out the repository.
2. Sets up the Godot export templates.
3. Builds the project for Windows, Linux, and Web.
4. Uploads the build artifacts.
5. Deploys the builds to itch.io using the Butler tool.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

- [Godot Engine](https://godotengine.org/)
- [GitHub Actions](https://github.com/features/actions)
- [itch.io](https://itch.io/)
