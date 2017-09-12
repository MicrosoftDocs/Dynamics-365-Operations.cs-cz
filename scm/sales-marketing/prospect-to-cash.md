---
title: "Zpeněžnění potenciálního zákazníka"
description: "Toto téma uvádí přehled řešení Zpeněžnění potenciálního zákazníka mezi aplikacemi Dynamics 365 for Sales and Dynamics 365 for Finance a Operations, Enterprise edition."
author: YuyuScheller
manager: AnnBe
ms.date: 07/12/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: YuyuScheller
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 2c82cc2cb88828e1828ce227e8c3ccd457a3df4d
ms.contentlocale: cs-cz
ms.lasthandoff: 07/27/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="39040-103">Zpeněžnění potenciálního zákazníka</span><span class="sxs-lookup"><span data-stu-id="39040-103">Prospect to cash</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="39040-104">Řešení Zpeněžnění potenciálního zákazníka používá [Integrátor dat](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration) k synchronizaci dat mezi instancemi aplikací Dynamics 365 Finance and Operations nebo Dynamics 365 for Sales prostřednictvím společných datových služeb.</span><span class="sxs-lookup"><span data-stu-id="39040-104">The Prospect to cash solution uses [Data Integrator](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration) to synchronize data across Dynamics 365 Finance and Operations or Dynamics 365 for Sales instances via the Common Data Service.</span></span> <span data-ttu-id="39040-105">Šablony Zpeněžnění potenciálního zákazníka dostupné v rámci Integrátoru dat umožňují tok produktů, účtů, kontaktů a dat prodejních kvót mezi aplikacemi Dynamics 365 for Finance a Operations a Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="39040-105">The Prospect to cash templates available with the Data Integrator enable the flow of product, account, contact, and sales quote data between Dynamics 365 for Finance and Operations and Dynamics 365 for Sales.</span></span> <span data-ttu-id="39040-106">V průběhu toku dat mezi aplikacemi Finance and Operations a Dynamics 365 for Sales můžete provádět prodejní a marketingové aktivity v aplikaci Dynamics 365 for Sales a zpracovávat plnění objednávky v rámci správy skladů v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="39040-106">While the data is flowing between Finance and Operations and Dynamics 365 for Sales, you can carry out sales and marketing activities in Dynamics 365 for Sales and handle the order fulfillment with inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="39040-107">Toto řešení umožňuje integraci v rámci následujících oblastí:</span><span class="sxs-lookup"><span data-stu-id="39040-107">This solution provides integration in the following areas:</span></span> 

-   <span data-ttu-id="39040-108">Správa účtů v aplikaci Dynamics 365 for Sales a jejich synchronizace v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="39040-108">Maintain accounts in Dynamics 365 for Sales and sync them to Finance and Operations.</span></span>
-   <span data-ttu-id="39040-109">Správa kontaktů v aplikaci Dynamics 365 for Sales a jejich synchronizace v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="39040-109">Maintain contacts in Dynamics 365 for Sales and sync them to Finance and Operations.</span></span>
-   <span data-ttu-id="39040-110">Vytvoření prodejních nabídek v aplikaci Dynamics 365 for Sales a jejich synchronizace v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="39040-110">Create sales quotes in Dynamics 365 for Sales and sync them to Finance and Operations.</span></span>
-   <span data-ttu-id="39040-111">Správa produktů v aplikaci Finance and Operations a jejich synchronizace s aplikací Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="39040-111">Maintain products in Finance and Operations and sync them to Dynamics 365 for Sales.</span></span>


