## Learn About Azure Storage 
Azure storage services provides a way to store different type of data securily. It is broken down into different storage servicies namely:
- Azure Blob Storage (Azure Blobs) - This is a storage service for unstructured data like pictures, videos, music files, documents, raw data. It follows 
a directory-like structure called a container

- Azure File Storage (Azure Files) - This is meant for VM's and services to share file storage. On-prem can also access this file using File Service REST API

- Azure Queue Storage (Azure Queues) - Like the name implies. It saves data in the first in and first out method. It is mostly used for logging, Typical use cases of Queue Storage include processing backlog messages or exchanging messages between Azure Web roles and Worker roles
- Azure Table Storage (Azure Tables) - This is ideal for key-value NoSQL data storage. it is schema-less and accessed via a REST API. Azure Table Storage is now part of Azure Cosmos DB.
- Azure Disk Storage (Azure Disks) - These are virtual hard disks. The available types of disks are ultra disks, premium solid-state drives (SSD), standard SSDs, and standard hard disk drives (HDD)

### Azure Storage Account Overview
An Azure Storage Account can be considered as a container that combines a set of Azure Storage services together. Integrating data services into a storage account allows you to manage them as a group. 

### Walkthrough
- Created a storage account 
![storage account](./images/storage-account.png)
- Created a container, uploaded an image into a folder called securitytest
![blob](./images/container-blob.png)
- Generated a SAS(shared access) URL
    ```
    https://uniquestorageaccname4.blob.core.windows.net/data/securitytest/fedora-iot-os.png?sp=r&st=2024-03-19T07:47:03Z&se=2024-03-21T15:47:03Z&sv=2022-11-02&sr=b&sig=rKjiG5UCJiBGX5Jx0hgn04QGYgBgKdLbS9xFV4LAkPw%3D
    ```
-  Created an azure file share and uploaded an image file
![file share](./images/file-share.png)
- Created a virtual network and attached it to the storage account
![virtual networl](./images/storage-accont-vnet.png)