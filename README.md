# Decode Morse

> Decode Morse, we built it using some methods in ruby to decode the morse code into letter.

## Set-up Rubocop GitHub Action

[Rubocop](https://www.rubocop.org/) is a Ruby static code analyzer (a.k.a. linter) and code formatter. It will enforce many of the guidelines outlined in the community [Ruby Style Guide](https://rubystyle.guide/).

This GitHub Action is going to run [Rubocop](https://docs.rubocop.org/en/stable/) to help you find style issues.

Please do the following **steps in this order**:

1. In the first commit of your feature branch create a `.github/workflows` folder and add a copy of [`.github/workflows/linters.yml`](.github/workflows/linters.yml) to that folder.
    - **Remember** to use the file linked above
    - **Remember** that `.github` folder starts with a dot.
2. **Do not make any changes in config files - they represent style guidelines that you share with your team - which is a group of all Microverse students.**
    - If you think that change is necessary - open a [Pull Request in this repository](../README.md#contributing) and let your code reviewer know about it.
3. When you open your first pull request you should see the result of the GitHub Actions:

![gh actions checks](../assets/images/gh-actions-rubocop-linters-checks.png)

Click on the `Details` link to see the full output and the errors that need to be fixed:

![gh actions failing checks](../assets/images/gh-actions-rubocop-failing-checks.png)

## [OPTIONAL]Set-up RSpec GitHub Action

You can run your tests with GitHub Actions to ensure that they are passing before merging a PR.

To use the GitHub Action to run your tests, please do the following **steps in this order**:

1. Add a copy of [`.github/workflows/tests.yml`](.github/workflows/tests.yml) to your `.github/workflows` folder.
    - **Remember** to use the file linked above
    - Do not modify or delete the [`.github/workflows/linters.yml`](.github/workflows/linters.yml) file that should already be in that folder.
    - RSpec by default will try to run any file ending in `_spec.rb` inside the `spec` folder. Make sure to follow this convention for your tests files so `rspec` can run your spec files.
    - You can modify the [`.github/workflows/tests.yml`](.github/workflows/tests.yml) file to better fit your custom needs.
3. When you open your pull request you should see the result of the GitHub Action:

![gh actions checks](../assets/images/gh-actions-rspec-tests-checks.png)

Click on the `Details` link of the test action to check the results of your tests.

## Set-up linters in your local env

### [RuboCop](https://docs.rubocop.org/en/stable/)

1. Add this line to the `Gemfile`
    ```
    gem 'rubocop', '>= 1.0', '< 2.0'
    ```
    *not sure how to use Gemfile? Read [this](https://bundler.io/v1.15/guides/bundler_setup.html).*
2. Run `bundle install`.
3. Copy [.rubocop.yml](./.rubocop.yml) to the root directory of your project
4. **Do not make any changes in config files - they represent style guidelines that you share with your team - which is a group of all Microverse students.**
    - If you think that change is necessary - open a [Pull Request in this repository](../README.md#contributing) and let your code reviewer know about it.
5. Run `rubocop`.
6. Fix linter errors.
7. **IMPORTANT NOTE**: feel free to research [auto-correct options for Rubocop](https://rubocop.readthedocs.io/en/latest/auto_correct/) if you get a flood of errors but keep in mind that correcting style errors manually will help you to make a habit of writing a clean code!

## Troubleshooting

- While using Colorize gem, if you are facing errors with Rspec related to 
    ```bash
    LoadError:
    cannot load such file -- colorize
    ```
    please remove ```--deployment``` from line no. [26](https://github.com/shubham14p3/Ruby-capstone-project/blob/ca86784cc88bea7c933e329c0953f07e21bcf6ca/.github/workflows/tests.yml#L16) of test.yml file.


## Author

👤 **Bandonkeye Arnaud**

- GitHub: [@githubhandle](https://github.com/ArnaudBand)
- Twitter: [@twitterhandle](https://twitter.com/@ba104781)
- LinkedIn: [LinkedIn](https://www.linkedin.com/in/ArnaudBandonkeye/)

👤 **Emmanuel Orji-Ihuoma**

GitHub: [@emmiiorji](https://github.com/ArnaudBand)
Twitter: [@emmiiorji](https://twitter.com/@emmiiorji)
LinkedIn: [LinkedIn](https://www.linkedin.com/in/orji-emmanuel)


## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

Feel free to check the [issues page](../../issues/).

## Show your support

Give a ⭐️ if you like this project!

## Acknowledgments

- Hat tip to anyone whose code was used
- Inspiration
- etc

## 📝 License

This project is [MIT](./MIT.md) licensed.