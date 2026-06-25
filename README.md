# Azure-ADF-Airport-Data-Pipeline
Metadata-driven Azure Data Factory pipeline for automated airport CSV ingestion, validation, archiving, error handling, and event-triggered processing.
# Azure Data Factory - Airport Data Pipeline

## Overview

This project demonstrates a metadata-driven Azure Data Factory (ADF) pipeline that automatically processes airport CSV files using event-based triggers.

Whenever a CSV file is uploaded into Azure Data Lake Storage Gen2, the pipeline automatically validates, processes, archives, and deletes the source file.

---

## Features

- Metadata-driven architecture
- Event Trigger (Automatic execution)
- Master-Child pipeline design
- Dynamic folder processing
- File validation
- Automatic archive
- Error handling
- Source file cleanup
- Azure Data Lake Storage Gen2

---

## Technologies Used

- Azure Data Factory
- Azure Data Lake Storage Gen2
- Azure Blob Events
- Azure Storage Account

---

## Pipeline Workflow

1. Upload CSV into Airport Landing Container
2. Event Trigger starts Master Pipeline
3. Master Pipeline reads available folders
4. Child Pipeline processes every file
5. Validate file
6. Copy valid files to Processed Container
7. Archive processed files
8. Delete source file
9. Invalid files move to Error Container

---

## Folder Structure

airport-landing/
    flights/
    passengers/
    staff/
    baggage/
    aircraft/

↓

airport-processed/

↓

airport-archive/

↓

airport-error/

---

## Pipeline Architecture

See Architecture folder.

---

## Sample Files

Sample CSV files are available inside Sample_Data folder.

---

## Screenshots

Project screenshots are available inside Screenshots folder.

---

## Future Improvements

- Duplicate Detection
- Logging
- Email Notifications
- Azure SQL Metadata Table
- Databricks Integration

---

