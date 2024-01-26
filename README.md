# 🚚 Data Migration: PostgreSQL to Snowflake 🌨️

## Overview

This repository contains a script to facilitate the migration of tables from a PostgreSQL database to a Snowflake account. The script automates the transfer process, ensuring a seamless transition of data.

## Repository Contents

- **data_transfer.sh:** Shell script to export data from PostgreSQL and upload it to Snowflake.

## Prerequisites

Before using the script, ensure the following prerequisites are met:

1. PostgreSQL installed and accessible.
2. Snowflake account with required credentials.
3. SnowSQL installed for Snowflake command-line operations.

## Usage

1. Modify the script's configuration section to include your PostgreSQL and Snowflake connection details.
2. Execute the script: `./data_transfer.sh`

## Script Details

The script performs the following steps:

1. Exports data from PostgreSQL table to a local CSV file.
2. Uploads the CSV file to Snowflake's internal stage.
3. Creates a Snowflake table with the same structure.
4. Copies data from the internal stage to the Snowflake table.

## Automation

To automate the data migration process, you can use tools like cron jobs or task schedulers. For example, to run the script every day at 2 AM:

```bash
0 2 * * * /path/to/data_transfer.sh

