[![CI](https://github.com/nogibjj/ids-706-w7-jingxuan-li/actions/workflows/CI.yml/badge.svg)](https://github.com/nogibjj/ids-706-w7-jingxuan-li/actions/workflows/CI.yml)

# Rust CLI Binary with SQLite
## What the project does
The project is a command-line interface (CLI) tool written in Rust, designed to perform SQLite operations. Its main features include:
1. Rust and SQLite: Utilizes Rust's performance and safety to handle SQLite database operations.
2. Command-Line Interface: Provides a user-friendly command-line options and help menu using the clap library.
3. Build and Run: Managed with Cargo, supporting code checks, builds, tests, formatting, and linting.
4. CI/CD Integration: Configured with GitHub Actions to automatically run CI/CD processes on every push to the main branch or pull request submission.
Users can execute database operations through simple commands, such as creating tables, loading data, and querying data.

## File Structure

- `sqlite/Makefile`: Makefile used for the `sqlite` project.
- `.github/workflows/CI.yml`: GitHub Actions CI configuration file.
- `sqlite/Cargo.toml`: Configuration file for the `sqlite` project.
- `.devcontainer/Dockerfile`: Dockerfile for setting up the development environment.
- `.devcontainer/devcontainer.json`: Devcontainer configuration file.
- `.gitignore`: Git ignore file, ignoring the `target/` directory.
- `sqlite/src/main.rs`: Main program file for the `sqlite` project.
- `sqlite/src/lib.rs`: Library file for the `sqlite` project.
- `sqlite/tests/tests.rs`: Test file for the `sqlite` project.
- `sqlite/data`: store the data file for the `sqlite` project.
## Running the Project

### Dependencies

- Install the Rust toolchain
- Install Docker (optional)

### How to run code

You can use Cargo to manage the build and execution process:

1. **Install Cargo if you haven't already**
    ```bash
    curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
    ```
    ```bash
    cargo --version
    ```
2. **Check the Code**
    ```bash
    cargo check
    ```
3. **Build the Project**
    ```bash
    cargo build
    ```
4. **Test the Project**
    ```bash
    cargo test
    ```
5. **Format the Code**
    ```bash
    cargo fmt
    ```
6. **Lint the Code**
    ```bash
    cargo clippy
    ```
7. **Build for Release**
    ```bash
    cargo build --release
    ```


This project uses Rust to perform SQLite operations and includes CLI (Command-Line Interface) features.

See `main.rs` for a commented example of how we create our CLI. By using `clap` over standard library options (such as `std::env` for Rust or `argparse` for Python), we gain a lot of free functionality like help menu guides.

Add the compiled binary (`--release`) to your path, allowing you to use your CLI normally without needing to run:

```bash
cargo run -- -<flag> argument
```

Instead, you can use:

```bash
sqlite -c table
```

Command to add the compiled binary to the path for use:

*If in Codespaces*

```bash
export PATH=$PATH:/workspaces/<REPO_NAME>/sqlite/target/release
```


### CRUD operation
- `sqlite -c table1` Create table `table1`.
- `sqlite -l table1 ../data/RestaurantReviews.csv` Load data into table `table` from `../data/customer_new.csv`.
- `sqlite -q "SELECT * FROM table1;"` Query: `SELECT * FROM table;`
- `sqlite -u table1 1 5` update id 1's restaurant score to be 5
- `sqlite -d table1` Drop table `table`.

### Use of LLM
1. **Finding Rust Knowledge**: 
   - ChatGPT provide me with resources, tutorials, and documentation related to Rust programming. For example, it can suggest official Rust documentation, online courses, and community forums where I learn about Rust concepts, syntax, and best practices.

2. **Debugging Code**: 
   - When I provide a snippet of Rust code that contains errors, ChatGPT can analyze the code, identify potential issues, and suggest fixes. It can explain the error messages I encounter and guide I through the debugging process step-by-step, helping me understand the underlying problems.

3. **Generating Rust Binary**: 
   - ChatGPT can explain the process of compiling Rust code into a binary executable. It can provide commands for using Cargo (Rust's package manager and build system) to build my project, including how to run `cargo build` and `cargo run` to generate and execute the binary. Additionally, it can explain how to set up my `Cargo.toml` file for dependencies and project configuration.



### Binary Download Link
[Download Link](https://github.com/nogibjj/ids-706-w7-jingxuan-li/actions/runs/11491604094/artifacts/2096849372)



### CI/CD

The project is configured with GitHub Actions, and the CI/CD process will automatically run on every push to the `main` branch or when a pull request is submitted. The CI configuration file is located at `.github/workflows/CI.yml`.

### Video link
