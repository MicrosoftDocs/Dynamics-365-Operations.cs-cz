---
title: Ohlášení za dokončené pro umístění bez řízení na základě registračních značek ze zařízení s kartou úlohy
description: V tomto tématu je popsán postup při dokončování hotových produktů ve výrobní zakázce do skladu, pokud registrační značka řídí dané skladové místo.
author: johanhoffmann
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: 35ad27a6b8a52bfd086fbe4fc57b1681ff88fd5b
ms.sourcegitcommit: 58db26b7edf02e7c33aaaf1c934e3263aa74b01f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/11/2019
ms.locfileid: "1995135"
---
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a><span data-ttu-id="d7e30-103">Ohlášení za dokončené pro umístění bez řízení na základě registračních značek ze zařízení s kartou úlohy</span><span class="sxs-lookup"><span data-stu-id="d7e30-103">Report as finished to a license plate controlled location from the Job card device</span></span> 

<span data-ttu-id="d7e30-104">Proces s názvem Hlášení jako dokončené dokončuje dokončené produkty ve výrobní zakázce do skladu.</span><span class="sxs-lookup"><span data-stu-id="d7e30-104">The process called Reporting as finished completes finished products on a production order to the inventory.</span></span> <span data-ttu-id="d7e30-105">Je-li dokončený produkt povolen pro rozšířené skladové procesy, produkt je hlášen jako dokončený do skladového místa s názvem výrobního výstupu.</span><span class="sxs-lookup"><span data-stu-id="d7e30-105">If the finished product is enabled for the advanced warehouse processes, the product is reported as finished to a location called the production output location.</span></span> <span data-ttu-id="d7e30-106">Další informace o nastavení skladového výstupu naleznete v tématu [místo výstupu ve výrobě](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span><span class="sxs-lookup"><span data-stu-id="d7e30-106">For information about setting up the production output location, see [Production output location](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).</span></span>

<span data-ttu-id="d7e30-107">Chcete-li dokončit tento úkol, je nutné vybrat existující číslo registrační značky.</span><span class="sxs-lookup"><span data-stu-id="d7e30-107">You must select an existing license plate number to complete this task.</span></span> <span data-ttu-id="d7e30-108">Je-li výstupní místo výroby nastaveno tak, aby bylo sledováno podle registrační značky, musí být při vykazování produkčního výstupního místa jako dokončené zahrnuto číslo registrační značky.</span><span class="sxs-lookup"><span data-stu-id="d7e30-108">If the production output location is set up to be tracked by license plate, then a license plate number must be included when reporting the production output location as finished.</span></span> <span data-ttu-id="d7e30-109">Pole **Registrační značka** je zobrazeno na výzvě **Průběh sestavy** na stránce **Zařízení karty úlohy**.</span><span class="sxs-lookup"><span data-stu-id="d7e30-109">The **License plate** field is visible on the **Report progress** prompt on the **Job card device** page.</span></span> <span data-ttu-id="d7e30-110">Toto pole je viditelné ve výzvě **Průběh sestavy** při vykazování poslední operace výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="d7e30-110">The field is only visible on the **Report progress** prompt when reporting on the last operation of the production order.</span></span> <span data-ttu-id="d7e30-111">Toto pole se zobrazí pouze v případě, že je pro procesy správy skladu povolena položka pro výrobní zakázku.</span><span class="sxs-lookup"><span data-stu-id="d7e30-111">The field is only shown if the item for the production order is enabled for the warehouse management processes.</span></span> 
