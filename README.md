## 🧪 Running Locally

### 1️⃣ Prerequisites
- Visual Studio 2022  
- Azure Functions Core Tools  
- Azure Storage Emulator or Azure Account  
- Azure Storage Explorer  

### 2️⃣ Setup

1. Clone the repository  
   git clone https://github.com/Singh-Neha-ST10433945/ST10433945_CLDV6212_POE_Part2.git  

2. Open the solution in Visual Studio.  

3. Configure the connection strings:  
   - In **local.settings.json**, set  
     "AzureWebJobsStorage": "<your-Azure-storage-connection-string>"  

   - In **appsettings.json**, verify the Functions base URL  
     "Functions": { "BaseUrl": "http://localhost:7027" }  

4. Run both projects in order:  
   - Start **ABCRetailersFunctions** first.  
   - Then start **ABCRetailers (MVC)**.  

---

## 🚀 Deployment to Azure

1. Publish both apps to **Azure App Service** using Visual Studio.  
2. In the **Azure Portal**, under each App Service, go to:  
   Configuration → Application Settings → Add the following:  

   Name: AzureWebJobsStorage  
   Value: <your Azure Storage connection string>  

3. Ensure that all **Tables**, **Blobs**, and **Queues** are under the same Storage Account.  

Once deployed, both the MVC front-end and the Azure Function App will interact through shared Azure resources.
