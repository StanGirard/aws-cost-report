# Pricy


## Install

```bash
brew tap stangirard/tap
brew install pricy
```

## Run

```bash
pricy
```

If you are using sso for credentials on aws

```bash
pricy --sso
```

## Usage

There are a couple of parameters that you can use
- `--details`: Show the details of the report with the pricing by service
- `--sso`: Use sso for credentials
- `--csv`: Output the report as csv to `reports.csv`
- `--evolution`: Show the evolution of the report as `evolution.csv`
- `--days`: Number of days to look back for
- `--interval`: Date Interval on which the report is generated (Default last 14 days) (Format: YYYY-MM-DD:YYYY-MM-DD)
- `--granularity`: Granularity of the report, can be `daily`,  `monthly`

## Example

### Report Generation

```bash
pricy --sso --granularity monthly --details
```

Generates a report for the price since the beginning last week with granularity of a month

<p align="center">
<img src="docs/aws-reports-granularity-month-details.png" alt="aws-reports-granularity-month-details" width="40%">
<p align="center">

### CSV Generation

```bash
pricy --sso --granularity monthly --month  --csv
```

Generates a csv report for the price  from one month ago

<p align="center">
<img src="docs/csv-aws-reports-granularity-month-details-month.png" alt="csv-aws-reports-granularity-month-details-month" width="40%">
<p align="center">