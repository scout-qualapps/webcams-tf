


## DBT Template Files

The following DBT template files have been added to your repository in the `dbt/` folder:

### Successfully Added (15 files):
- `dbt/.gitignore`
- `Dockerfile`
- `dbt/README.md`
- `dbt/dbt_project.yml`
- `dbt/schema.yml`
- `dbt/analyses/.gitkeep`
- `dbt/macros/.gitkeep`
- `dbt/models/datamart/model_dm.sql`
- `dbt/models/intermediate/model_interm.sql`
- `dbt/models/staging/model_stg.sql`
- `dbt/profiles/.user.yml`
- `dbt/profiles/profiles.yml`
- `dbt/seeds/.gitkeep`
- `dbt/snapshots/.gitkeep`
- `dbt/tests/.gitkeep`


---
### Next Steps: Update DBT Models for Data Transformations

**You must update the DBT models** in the `dbt/models/` folder to apply your data transformations. The template includes placeholder models that need to be customized for your use case.

#### Data Transformation Flow:
Data moves through the following layers in your dbt project:

1. **Raw Layer** → Data extracted from Airbyte (source tables)
2. **Staging Layer** (`dbt/models/staging/`) → Clean and standardize raw data
3. **Intermediate Layer** (`dbt/models/intermediate/`) → Business logic and joins
4. **Datamart Layer** (`dbt/models/datamart/`) → Final analytics-ready tables

**Example workflow:**
- Edit `dbt/models/staging/model_stg.sql` to reference your Airbyte raw tables
- Edit `dbt/models/intermediate/model_interm.sql` to add business transformations
- Edit `dbt/models/datamart/model_dm.sql` to create your final analytics tables

Refer to the [dbt documentation](https://docs.getdbt.com/) for guidance on writing models.

*This repository was created automatically.*
