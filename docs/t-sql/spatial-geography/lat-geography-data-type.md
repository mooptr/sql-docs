---
title: "Lat (geography Data Type) | Microsoft Docs"
ms.custom: ""
ms.date: "03/14/2017"
ms.prod: "sql-non-specified"
ms.prod_service: "database-engine, sql-database"
ms.service: ""
ms.component: "t-sql|spatial-geography"
ms.reviewer: ""
ms.suite: "sql"
ms.technology: 
  - "database-engine"
ms.tgt_pltfrm: ""
ms.topic: "language-reference"
f1_keywords: 
  - "Lat"
  - "Lat_TSQL"
dev_langs: 
  - "TSQL"
helpviewer_keywords: 
  - "Lat method"
ms.assetid: 051d66bc-04de-4c58-861c-760dc5b859b5
caps.latest.revision: 14
author: "BYHAM"
ms.author: "rickbyh"
manager: "jhubbard"
ms.workload: "Inactive"
---
# Lat (geography Data Type)
[!INCLUDE[tsql-appliesto-ss2008-asdb-xxxx-xxx-md](../../includes/tsql-appliesto-ss2008-asdb-xxxx-xxx-md.md)]

  The latitude property of the **geography** instance.  
  
## Syntax  
  
```  
.Lat  
```  
  
## Return Types  
 [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] type: **float**  
  
 CLR type: **SqlDouble**  
  
## Remarks  
 In the OpenGIS model, Lat is defined only on **geography** instances composed of a single point. This property will return NULL if **geography** instances contain more than a single point. This property is precise and read-only.  
  
## Examples  
 This example creates a point and returns the latitude of the point.  
  
```  
DECLARE @g geography;  
SET @g = geography::STGeomFromText('POINT(-122.34900 47.65100)', 4326);  
SELECT @g.Lat;  
```  
  
## See Also  
 [Extended Methods on Geography Instances](../../t-sql/spatial-geography/extended-methods-on-geography-instances.md)  
  
  
