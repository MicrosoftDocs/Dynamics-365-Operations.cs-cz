---
title: Synchronizace data a času v úlohách importu
description: Použijte časová pásma UTC v úlohách importu, abyste předešli problémům s převody časových pásem.
author: Sunil-Garg
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 41c0ec805a20a525989e0133e5dffb29ce3fed39
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748662"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a><span data-ttu-id="1a579-103">Synchronizace data a času v úlohách importu</span><span class="sxs-lookup"><span data-stu-id="1a579-103">Synchronize date and time in import jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1a579-104">Je důležité nastavit časové pásmo pro vaši úlohu importu na koordinovaný světový čas (UTC).</span><span class="sxs-lookup"><span data-stu-id="1a579-104">It's important to set the time zone for your import job to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="1a579-105">Pokud použijete jiné nastavení, mohou se v importovaných datech zobrazit neočekávaná data a časy.</span><span class="sxs-lookup"><span data-stu-id="1a579-105">You might see unexpected dates and times in your imported data if you use a different setting.</span></span> <span data-ttu-id="1a579-106">Bez správného nastavení převede proces importu datum UTC na místní formát a poté jej znovu převede systémové nastavení.</span><span class="sxs-lookup"><span data-stu-id="1a579-106">Without the correct setting, the import process converts the UTC date to the local format, and then system settings converts it again.</span></span>

<span data-ttu-id="1a579-107">Tato duální konverze způsobí změnu dat mezi aplikacemi.</span><span class="sxs-lookup"><span data-stu-id="1a579-107">This dual conversion causes dates to change between applications.</span></span> <span data-ttu-id="1a579-108">Například duální konverze může způsobit, že se počáteční datum zaměstnance bude lišit mezi Dynamics 365 Human Resources a Dynamics 365 Finance kvůli rozdílům v místních časových pásmech.</span><span class="sxs-lookup"><span data-stu-id="1a579-108">For example, the dual conversion could cause an employee's start date to be different between Dynamics 365 Human Resources and Dynamics 365 Finance due to differences in local time zones.</span></span> <span data-ttu-id="1a579-109">Nastavení úlohy importu na UTC tento problém řeší.</span><span class="sxs-lookup"><span data-stu-id="1a579-109">Setting the import job to UTC resolves this problem.</span></span>

1. <span data-ttu-id="1a579-110">V Dynamics 365 Finance and Operations vyberte **Správa dat**.</span><span class="sxs-lookup"><span data-stu-id="1a579-110">In Dynamics 365 Finance and Operations, select **Data management**.</span></span>

2. <span data-ttu-id="1a579-111">Vyberte **Importovat projekty** a poté vyberte projekt.</span><span class="sxs-lookup"><span data-stu-id="1a579-111">Select **Import projects**, and then select the project.</span></span>

3. <span data-ttu-id="1a579-112">V části **Formát data zdroje** vyberte **CSV-Unicode**.</span><span class="sxs-lookup"><span data-stu-id="1a579-112">Under **Source date format**, select **CSV-Unicode**.</span></span>

   <span data-ttu-id="1a579-113">[![Změna formátu zdrojového data na UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span><span class="sxs-lookup"><span data-stu-id="1a579-113">[![Change source date format to UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span></span>

4. <span data-ttu-id="1a579-114">Změňte **Časové pásmo** na **standard UTC (Coordinated Universal Time)** a změňte **Jazyk** na **En-US**.</span><span class="sxs-lookup"><span data-stu-id="1a579-114">Change **Timezone** to **Coordinated Universal Timezone**, and change **Language** to **En-US**.</span></span>




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]