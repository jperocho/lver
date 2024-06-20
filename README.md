# AWS Lambda Version Management Script

## Problem

In AWS Lambda, each account has a storage limit for all deployed functions. This includes both active and inactive versions of your Lambda functions. When the number of versions increases, you might hit the storage limit, which can prevent you from deploying new versions of your functions. To manage this, it’s essential to periodically clean up older versions, keeping only the necessary ones. This script automates the deletion of older Lambda function versions, ensuring that you stay within the storage limits.

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
./lver --serverless-yaml-path /path/to/serverless.yml
