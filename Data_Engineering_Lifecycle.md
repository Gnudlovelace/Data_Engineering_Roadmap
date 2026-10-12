# THE DATA ENGINEERING LIFECYCLE DESCRIBE THE PROCESS DATA GOES THROUGH, FROM ITS CREATION TO ITS UTILIZATION.

<img width="320" height="180" alt="image" src="https://github.com/user-attachments/assets/cd68e0ba-8a91-4d0d-b5aa-ec8a86a8d0e7" />

## -- Generation: Collecting data from various source systems. 
  
  ### - Source systems 
  
        + Are the origin points of data where we interact with these systems to collect raw data
        
        + Knowing how data is generated, its frequency, velocity, and variety is important for us to understand how source systems operate
        
        + Effective communication with source system owners is also crucial to manage changes that might affect data pipelines
    
  ### - Key considerations:
    
        + Data Characteristics: Is the source an application, IoT device, etc.?
      
        + Data Persistence: Is the data stored long-term or deleted quickly?
      
        + Data Generation Rate: How much data is generated over time?
      
        + Consistency: How reliable is the data quality?
      
        + Error Rates: Frequency of data errors.
      
        + Duplicates: Presence of duplicate data entries.
      
        + Schema: The structure of the ingested data.
      
        + Change Management: Handling schema changes and data updates.
      
        + Impact on Performance: How data reading affects source system performance.
        
  ### - Examples:
  
        + Traditional Application Databases
        
        + IoT Swarms

## -- Storage: Safely storing data for future processing and analysis.

  ### Importance of Storage

    - Data storage is a crucial stage in the data engineering lifecycle, the choice of storage solution significantly impact the efficiency of data
      
      processing,transformation, and serving
    
  ### Key Considerations
  
  When selecting a storage solution, data engineers must evaluate several key factors to ensure optimal performance and scalability:
    
    + Compatibility: Ensure the storage solution supports the required write and read speeds for your architecture.
    
    + Performance Bottlenecks: Assess if the storage system could create bottlenecks for downstream processes.
    
    + Understanding of Technology: Utilize the storage system optimally without committing antipatterns (e.g., high-rate random access updates in an object storage
      system).
      
    + Scalability: Consider the system’s ability to handle future scale in terms of storage capacity, read/write operation rates, etc.
    
    + Data Retrieval: Ensure downstream users can retrieve data within required service-level agreements (SLAs).
    
    + Metadata Management: Capture metadata about schema evolution, data flows, and data lineage to enhance data utility.
    
    + Query Capabilities: Determine if the storage solution supports complex query patterns or is purely for storage.
    
    + Schema Handling: Understand if the storage system is schema-agnostic, flexible schema, or enforced schema.
    
    + Data Governance: Track master data, golden records, data quality, and data lineage for regulatory compliance and data sovereignty.

  ### Data Access Frequency
  
  Determines the “temperature” of your data, influencing the choice of storage solution:

    + Hot Data: Frequently accessed data, needing fast retrieval, stored in high-speed storage solutions.

    + Lukewarm Data: Accessed occasionally, stored in moderately fast storage solutions.

    + Cold Data: Rarely accessed, suitable for archival storage solutions with lower retrieval costs but higher storage efficiency.

  ### Storage Solutions
  
  There are various storage solutions available, each suited to different data access patterns and use cases:
  
    + Cloud Data Warehouses: Offer scalable storage with integrated processing capabilities (e.g., Amazon Redshift, Google BigQuery).
    
    + Data Lakes: Allow storage of large volumes of raw data in its native format, supporting a wide range of data types (e.g., AWS S3, Azure Data Lake Storage).
    
    + Object Storage: Suitable for storing large amounts of unstructured data, often with built-in query capabilities (e.g., Amazon S3, Google Cloud Storage).
          
## -- Ingestion: Bringing data into a centralized system.

  ### Key Considerations

    + Use Cases: Identify the purpose of the ingested data and potential reuse scenarios.
    
    + Reliability: Ensure the source systems and ingestion processes are reliable and data is available when needed.
    
    + Data Destination: Determine where the ingested data will be stored and how it will be accessed.
    
    + Access Frequency: Understand how often the data will be accessed.
    
    + Data Volume: Assess the typical volume of incoming data.
    
    + Data Format: Ensure downstream systems can handle the ingested data format.
    
    + Data Quality: Evaluate the quality of source data and its suitability for immediate use.
    
    + Transformation Needs: Determine if data needs to be transformed before reaching its destination, including potential in-flight transformations.

  ### Batch vs. Streaming

  Data ingestion can be done in batch mode or as a continuous stream:
  
    + Batch Ingestion: Processes large chunks of data at scheduled intervals. Suitable for use cases where real-time processing is not required.

    + Streaming Ingestion: Provides data to downstream systems in near real-time. Ideal for scenarios requiring immediate data availability.

  ### Push vs. Pull Models

    + Pull Model: Target system retrieves data from source systems. Suitable for periodic data collection.

    + Push Model: Source systems write data directly to the target system. Useful when immediate data transfer is required.

## -- Transformation: Converting data into pretty format that is useful for analysis.

  ### Transformation Process

    + Data transformation involves converting raw data into a suitable format 
    
    + This stage is crucial for adding value to data and making it useful for downstream processes

  ### Key Considerations
  
  When planning data transformations, data engineers must consider:
  
    + Business Value: Assess the cost and ROI of the transformation processes.
    
    + Simplicity: Ensure transformations are as simple and self-contained as possible.
    
    + Business Rules: Incorporate business logic to ensure data transformations support organizational needs.

  ### Transformation Methods

    + Data Cleaning: Correcting or removing inaccurate records.

    + Schema Transformation: Changing the data schema to a more usable structure.

    + Normalization: Organizing data to reduce redundancy.

    + Aggregation: Summarizing data for reporting purposes.

    + Featurization: Extracting features for machine learning models.

## -- Serving Data: Providing data to end-users for decision-making and operational purposes.

  ### Purpose of Serving Data
  
    + Serving data involves providing processed data to end-users for decision-making, operational purposes, and advanced analytics. This is where the value of 
      data engineering efforts becomes evident.

  ### Types of Data Serving

    + Analytics: Business Intelligence (BI), Operational Analytics, Embedded Analytics

    + Machine Learning: Model Training, Real-time Prediction

    + Reverse ETL: Feeding Data Back

  ### 
                 

RECOMMEND TO READ: https://medium.com/towards-data-engineering/data-engineering-lifecycle-d1e7ee81632e
