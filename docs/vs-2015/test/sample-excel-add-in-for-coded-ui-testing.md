---
title: "Sample Excel Add-In for Coded UI Testing | Microsoft Docs"
ms.custom: ""
ms.date: 11/15/2016
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-devops-test"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "coded UI tests, Excel Add-in sample"
ms.assetid: 2cd52d1a-4c35-43ca-8a84-9c79dabd907f
caps.latest.revision: 18
ms.author: gewarren
manager: "douge"
---
# Sample Excel Add-In for Coded UI Testing
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

This sample Add-In for [!INCLUDE[ofprexcel](../includes/ofprexcel-md.md)] is designed specifically to support Coded UI Tests of Excel worksheets that are recorded and run in Visual Studio Enterprise. The Add-In is created by using Visual Studio Tools for Office.  
  
 For more information about how to create an Excel Add-In, see [Walkthrough: Creating Your First VSTO Add-in for Excel](http://msdn.microsoft.com/library/a855e2be-3ecf-4112-a7f5-ec0f7fad3b5f) or search MSDN for "Excel Add-In".  
  
 Although the Excel Add-In is not the primary subject of this documentation of the Coded UI Test Extension for Excel, a few comments may be helpful.  
  
 The important parts of this Add-In:  
  
-   `ThisAddIn`  Class - Manages the .NET Remoting channel between the `ExcelUICommunicator` and the [Sample Coded UI Test Extension for Excel](../test/sample-coded-ui-test-extension-for-excel.md).  
  
-   `ExcelCodedUIAddinHelper_TemporaryKey.pfx`  - A security certificate for testing the Add-In.  
  
-   `ExcelUICommunicator`  Class - This class implements the `IExcelUICommunication` interface.  
  
## ThisAddIn Class  
 Most of this class is actually generated by Visual Studio Tools for Office in the `ThisAddIn.Designer.cs` file when you create your Excel Add-In project.  
  
 The members that you must implement are the event handlers: `ThisAddIn_Startup()` and `ThisAddIn_Shutdown()`. Their purpose is to initialize or close the .NET Remoting channel that is used by the `ExcelUICommunicator`.  
  
## ExcelCodedUIAddinHelper_TemporaryKey.pfx  
 This file contains a temporary security certificate that is generated by Visual Studio Tools for Office and gives the Add-In assembly permission to operate in the Excel process for testing the Add-In and extension. You should delete this certificate and either create a new one in the **Signing** tab of the project **Properties** window, or attach your own testing certificate.  
  
## ExcelUICommunicator Class  
 This class implements the `IExcelUITestCommunication` interface and gets the requested UI information from the Excel object model. For more information, see [Sample Excel Communicator Interface](../test/sample-excel-communicator-interface.md).  
  
## See Also  
 [Extending Coded UI Tests and Action Recordings to Support Microsoft Excel](../test/extending-coded-ui-tests-and-action-recordings-to-support-microsoft-excel.md)   
 [Walkthrough: Creating Your First VSTO Add-in for Excel](http://msdn.microsoft.com/library/a855e2be-3ecf-4112-a7f5-ec0f7fad3b5f)   
 [Office and SharePoint Development](http://msdn.microsoft.com/library/2ddec047-263a-4901-a54c-a15fc8472329)



