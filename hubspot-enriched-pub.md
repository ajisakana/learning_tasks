# AI-Lab Data Ingestion

## Goal: To automatically update BigQuery Table whenever new file is pushed to GCS

### Steps
- Create a pub-sub topic hubspot-enriched-data
- Create a subscription gcs-pull-sub to view/consume messages
- Run import job from Dataflow template - Cloud Storage Text to Pub/Sub (Stream)
    - Use regex files pattern: </br>
    gs://aji-ailab-e-nb-asne1-ds-v1/companies_demo/hubspot*.csv </br>
- Check imported messages from previously created subscription gcs-pull-sub
- Run export job to BigQuery from template - Pub/Sub Topic to BigQuery
- Check logs from Dataflow jobs running
- View table and run queries from BigQuery to validate setup
