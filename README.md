# TrainingPlan407

[![Stable](https://img.shields.io/badge/docs-stable-blue.svg)](https://fieldofnodes.github.io/TrainingPlan407.jl/stable/)
[![Dev](https://img.shields.io/badge/docs-dev-blue.svg)](https://fieldofnodes.github.io/TrainingPlan407.jl/dev/)
[![Build Status](https://github.com/fieldofnodes/TrainingPlan407.jl/actions/workflows/CI.yml/badge.svg?branch=main)](https://github.com/fieldofnodes/TrainingPlan407.jl/actions/workflows/CI.yml?query=branch%3Amain)

# TrainingPlan407

Welcome to the `TrainingPlan407` module! This Julia package integrates functionality from several other modules (`BaseTrainingPlan`, `TrainingContent`, `TrainingLog`, `TrainingBook`, `TrainingPlan`, and `TrainingAssessment`) to provide a comprehensive toolset for managing training plans, logs, books, and assessments. This module streamlines the process of generating and exporting training-related documents in LaTeX format.

## Features

- **Module Generation**: Automatically generate training modules based on assessment data.
- **Training Table Data**: Create structured training table data from a list of content titles.
- **Document Export**: Export training logs, plans, books, and assessments as LaTeX files for easy integration into larger documents.
- **Assessment Tools**: Generate and export skill assessments, including results and detailed analyses.

## Installation

To use `TrainingPlan407`, ensure that you have Julia installed on your system. You can add this module to your Julia environment by including it in your project or environment:

```julia
] add https://github.com/your-repo/TrainingPlan407
```

## Usage

Begin by importing the module into your Julia environment:

```julia
using TrainingPlan407
```

### Generating Training Modules

To generate a list of training modules from an assessment file, use the `generate_modules` function:

```julia
modules = generate_modules("assessment_file.csv")
```

This function reads the specified CSV file, processes the assessment data, and returns a list of modules.

### Creating Training Table Data

To create structured training table data from a list of content titles, use the `generate_training_table_data` function:

```julia
ttd = generate_training_table_data(["Module 1", "Module 2", "Module 3"])
```

This returns a `TrainingTableData` object containing the training content.

### Writing Training Logs to File

To export a training log to a LaTeX file, use the `write_training_log_to_file` function:

```julia
write_training_log_to_file(ttd)
```

This writes the training log to a file named `training_log.tex`.

### Writing Training Plans to File

To export a training plan to a LaTeX file, use the `write_training_plan_to_file` function:

```julia
write_training_plan_to_file(ttd)
```

This writes the training plan to a file named `training_plan.tex`.

### Writing Training Book Lists to File

To generate and export a list of training book modules to a LaTeX file, use the `write_training_book_list_to_file` function:

```julia
write_training_book_list_to_file(ttd)
```

This writes the training book list to a file named `training_book.tex`.

### Writing Training Assessments to File

To export a training assessment to a LaTeX file, use the `write_training_assessment_to_file` function:

```julia
write_training_assessment_to_file(ttd)
```

This writes the training assessment to a file named `training_assessment.tex`.

### Writing Training Assessment Results to File

To generate and export a detailed skill assessment report to a LaTeX file, use the `write_training_assessment_results_to_file` function:

```julia
write_training_assessment_results_to_file("assessment_file.csv", ttd)
```

This writes the detailed assessment results to a file named `training_assessment_results.tex`.

### Example Usage

```julia
# Generate modules from an assessment file
modules = generate_modules("assessment_file.csv")

# Create training table data
ttd = generate_training_table_data(modules)

# Write various training-related documents to LaTeX files
write_training_log_to_file(ttd)
write_training_plan_to_file(ttd)
write_training_book_list_to_file(ttd)
write_training_assessment_to_file(ttd)
write_training_assessment_results_to_file("assessment_file.csv", ttd)
```

## Contributing

Contributions to `TrainingPlan407` are welcome! Please submit a pull request with your changes or open an issue if you encounter any problems.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For questions, suggestions, or feedback, feel free to reach out via [GitHub Issues](https://github.com/your-repo/TrainingPlan407/issues).

---

This README provides an overview of the functionality within `TrainingPlan407`. For detailed examples and additional information, please refer to the module's source code and documentation.
