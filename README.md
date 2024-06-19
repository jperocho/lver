# AWS Lambda Version Management Script

## Overview

This script helps manage AWS Lambda function versions by deleting older versions, keeping only the five most recent versions. It reads function definitions from a `serverless.yml` file.

## Setup

### Prerequisites

- Python 3.x
- AWS CLI configured with appropriate permissions
- `boto3` and `PyYAML` Python libraries

### Installation

1. Clone the repository or download the script.

2. Install the required Python libraries using pip:

    ```sh
    pip install boto3 pyyaml
    ```

## Usage

### Command-Line Arguments

- `--serverless-yaml-path`: Path to the `serverless.yml` file containing Lambda function definitions. This argument is required.

### Example Command

```sh
./lver --serverless-yaml-path ../../bluering-procurement-services/serverless.yml
