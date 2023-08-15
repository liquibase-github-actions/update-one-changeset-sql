# Liquibase Update One Changeset Sql Action
Official GitHub Action to run Liquibase Update One Changeset Sql in your GitHub Action Workflow. For more information on how update one changeset sql works visit the [Official Liquibase Documentation](https://docs.liquibase.com/commands/home.html).
## Update One Changeset Sql
[PRO]
Generates sql to run single changeset
## Usage
```yaml
steps:
- uses: actions/checkout@v3
- uses: liquibase-github-actions/update-one-changeset-sql@v4.23.1
  with:
    # Author of the changeset to execute
    # string
    # Required
    changesetAuthor: ""

    # Id of the changeset to execute
    # string
    # Required
    changesetId: ""

    # Path to the changeset to execute
    # string
    # Required
    changesetPath: ""

    # The JDBC database connection URL
    # string
    # Required
    url: ""

    # The default catalog name to use for the database connection
    # string
    # Optional
    defaultCatalogName: ""

    # The default schema name to use for the database connection
    # string
    # Optional
    defaultSchemaName: ""

    # The JDBC driver class
    # string
    # Optional
    driver: ""

    # The JDBC driver properties file
    # string
    # Optional
    driverPropertiesFile: ""

    # Password to use to connect to the database
    # string
    # Optional
    password: ""

    # Username to use to connect to the database
    # string
    # Optional
    username: ""

```

### Secrets
It is a good practice to protect your database credentials with [GitHub Secrets](https://docs.github.com/en/actions/security-guides/encrypted-secrets)

## Optional Liquibase Global Inputs
The liquibase update one changeset sql action accepts all valid liquibase global options as optional parameters. A full list is available in the official [Liquibase Documentation](https://docs.liquibase.com/parameters/command-parameters.html).

### Example
```yaml
steps:
  - uses: actions/checkout@v3
  - uses: liquibase-github-actions/update-one-changeset-sql@v4.23.1
    with:
      changesetAuthor: ""
      changesetId: ""
      changesetPath: ""
      url: ""
      headless: true
      licenseKey: ${{ secrets.LIQUIBASE_LICENSE_KEY }}
      logLevel: INFO
```

## Feedback and Issues
This action is automatically generated. Please submit all feedback and issues with the [generator repository](https://github.com/liquibase/github-action-generator/issues).
