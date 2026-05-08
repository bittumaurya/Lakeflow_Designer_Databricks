# Lakeflow Designer Project

A Databricks Lakeflow Designer project that demonstrates an end-to-end data pipeline using the medallion architecture pattern. The workflow ingests raw source files, transforms them through bronze and silver layers, and produces a final gold-layer output for analytics and reporting.

![Lakeflow Designer Workflow](Project_screenshotS/Lakeflow_Designer_View.png)

## About Lakeflow Designer

Lakeflow Designer is a visual, no-code, AI-native experience in Databricks that helps users build data preparation and analytics workflows using a drag-and-drop canvas and natural language support. It is designed to make data workflows easier to create, understand, and maintain while still staying governed and production-ready through Unity Catalog. [web:793][web:787]

![Lakeflow Designer Interface](https://pplx-res.cloudinary.com/image/upload/pplx_search_images/7b9a67270fc682280a715166f92f5679d782eeab.jpg)

Lakeflow Designer is useful because it lets you visually organize a data pipeline from ingestion to transformation to output, instead of writing every step manually. This is especially helpful for ETL and ELT workflows, where clarity, modularity, and governance matter. [web:793][web:787]

![Medallion Architecture](https://pplx-res.cloudinary.com/image/upload/pplx_search_images/5954c8873ba84456e275153d6aa5e7a8e3b3cb9b.jpg)

The medallion approach used in this project follows the common Bronze, Silver, and Gold layers pattern. Bronze stores raw ingested data, Silver contains cleaned and transformed data, and Gold contains business-ready output for analytics. [web:788][web:786]

## Project Overview

This project shows how Lakeflow Designer can be used to build a structured data pipeline in Databricks. The workflow is designed around source ingestion, transformation, joins, and final curated output using a layered architecture.

## Folder Structure

```text
databricks_files/
└── lakeflow_designer.ipynb

project_screenshot/
└── lakeflow_designer/
    └── Lakeflow_Designer_View.jpg

catalog_structure/

source_data/
├── product/
├── orders/
├── region/
└── city/
```

## Data Sources

The source data used in this project includes:
- `product`
- `orders`
- `region`
- `city`

These source files are used to build the raw ingestion layer and support the downstream transformations in Bronze, Silver, and Gold stages.

## Workflow Design

### Raw Layer
This is where the source files are first read into the pipeline.

### Bronze Layer
In this layer, the raw data is converted into Delta format and stored in a cleaner, more manageable structure.

### Silver Layer
This stage performs transformations such as cleaning columns, combining datasets, and preparing data for joins.

### Gold Layer
The final layer contains enriched and analytics-ready data for reporting and downstream use.

## What I Built

In this project, I built a Lakeflow Designer pipeline with:
- Raw data ingestion from source files.
- Bronze layer Delta conversion.
- Silver layer transformations and joins.
- Gold layer final output creation.
- A visual workflow organized in a clean multi-layer design.

## Screenshot Preview

This screenshot shows the full Lakeflow Designer workflow created in Databricks:

![Lakeflow Designer Project Screenshot](project_screenshots/Catalog_Structure.png)

## Key Learnings

This project helped me understand:
- How Lakeflow Designer works in Databricks.
- How to design ETL pipelines visually.
- How medallion architecture improves pipeline organization.
- How raw data moves through bronze, silver, and gold layers.
- How to structure a project for clarity and maintainability.

## Why Lakeflow Designer Matters

Lakeflow Designer is valuable because it reduces the complexity of pipeline creation while keeping the workflow production-oriented. It helps bridge the gap between technical and non-technical users, while still supporting governance, scalability, and maintainability. [web:793][web:787]

## Conclusion

This project is a practical example of building a modern Databricks workflow using Lakeflow Designer and medallion architecture. It shows how raw data can be transformed into reliable business-ready output through a clear and scalable pipeline design.

## References

- Databricks Lakeflow Designer: https://learn.microsoft.com/en-us/azure/databricks/designer/
- Databricks Medallion Architecture: https://docs.databricks.com/aws/en/lakehouse/medallion
- Databricks Lakeflow Designer announcement: https://www.databricks.com/company/newsroom/press-releases/databricks-unveils-lakeflow-designer-data-analysts-build-reliable