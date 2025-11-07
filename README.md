# PS 2 Ex 3

# Setup

## Envrionment

Install the required packages by running:

```bash
conda env create -f environment.yml
```

Activate the environment by running:

```bash
conda activate solution_ps2_ex3_database
```

## Pre-commit

This repository uses pre-commit to run some checks before each commit. To install pre-commit, run:

```bash
pre-commit install
```

To run the checks manually, run:

```bash
pre-commit run --all-files
```

# Getting the data

1. create a Kaggle account: https://www.kaggle.com/
2. get API keys and user name
   - Go to your account, and click on your profile in the top right
   - Then click on "Settings"
   - Scroll down to the API section and click on "Create New Token"
   - Get your username and API key from there

We have written a data loader function for you in the "nba/data_loader.py".This allows you to
download the data with by running the script from the terminal. Run the following command in the
terminal being at the root of the repository.

```bash
python nba/data_loader.py -u "your_user_name" -k "your_api_key" -d "wyattowalsh/basketball"
```

Replace "your_user_name" and "your_api_key" with your username and API key. This creates a json
file at "~/.kaggle/kaggle.json" with your username and API key, which is used to authenticate your
account and download the data.


# Answers to question 2
# purpose of if __name__ == "__main__":
#    main()
''' makes sure to only run the main function if file is run directly, and ensure it is not run automatically when imported i.e.
stops data loading process being run automatically when other files import functions from it"
# Answers to question 3 - how the click package enables command line fuctionality
'''
in data_loader using @click.option and @click.command enables command line functionality by defining the command-line arguments the function accepts, and e.g. with required=True, shows an error if it does not provide a required argument, and using help allows the user to wiew the help menu for the command.
Click parses the terminal imput and validates it, and then passes the values into the main function as parameters therefore enabling command line interface functionality
'''
