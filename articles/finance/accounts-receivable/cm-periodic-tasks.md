---
title: Pravidelné úlohy správy úvěrů
description: V tomto tématu jsou popsány pravidelné úlohy, které jsou nezbytnou součástí procesu správy limitů úvěru u odběratelů.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: df3b0b239fe542eab80fa92057248328d3f5188f
ms.sourcegitcommit: 6a70f9ac296158edd065d52a12703b3ce85ce5ee
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3015148"
---
# <a name="periodic-credit-management-tasks"></a><span data-ttu-id="3e16b-103">Pravidelné úlohy správy úvěrů</span><span class="sxs-lookup"><span data-stu-id="3e16b-103">Periodic credit management tasks</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="3e16b-104">V tomto tématu jsou popsány pravidelné úlohy, které jsou nezbytnou součástí procesu správy limitů úvěru u odběratelů.</span><span class="sxs-lookup"><span data-stu-id="3e16b-104">This topic describes the periodic tasks that are a necessary part of the process of managing credit limits for customers.</span></span>

## <a name="update-risk-scores"></a><span data-ttu-id="3e16b-105">Aktualizovat skóre rizika</span><span class="sxs-lookup"><span data-stu-id="3e16b-105">Update risk scores</span></span>

<span data-ttu-id="3e16b-106">Během vývoje podniku a při změnách okolností se mohou měnit také úvěrová rizika u daného odběratele.</span><span class="sxs-lookup"><span data-stu-id="3e16b-106">As businesses evolve and circumstances change, the credit risks for a given customer can also change.</span></span> <span data-ttu-id="3e16b-107">Chcete-li pro odběratele zachovat odpovídající limity úvěru, je nutné pravidelně kontrolovat kritéria pro jednotlivá hodnocení rizik a aktualizovat hodnocení jednotlivých odběratelů.</span><span class="sxs-lookup"><span data-stu-id="3e16b-107">To help maintain appropriate credit limits for your customers, you must periodically review the criteria for each risk score and update the scores for each customer.</span></span> <span data-ttu-id="3e16b-108">Následující hodnocení lze aktualizovat pomocí stránky **Aktualizace hodnocení rizik** (**Úvěr a inkasa \> Pravidelné úlohy \> Správa úvěru \> Aktualizace hodnocení rizik**).</span><span class="sxs-lookup"><span data-stu-id="3e16b-108">You can update the following scores by using the **Update risk scores** page (**Credit and collections \> Periodic tasks \> Credit management \> Update risk scores**).</span></span> <span data-ttu-id="3e16b-109">Jsou také zpracovány všechny výpočty definované uživatelem.</span><span class="sxs-lookup"><span data-stu-id="3e16b-109">All user-defined calculations are also processed.</span></span>

- <span data-ttu-id="3e16b-110">**Průměrný počet dnů do zaplacení** – Toto hodnocení je průměrný počet dnů do zaplacení faktur odběratelem.</span><span class="sxs-lookup"><span data-stu-id="3e16b-110">**Average payment days** – This score is the average number of days that a customer takes to pay invoices.</span></span>
- <span data-ttu-id="3e16b-111">**Odběratelem od** – Toto hodnocení představuje počet let, po který byl odběratel odběratelem vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="3e16b-111">**Customer since** – This score is the number of years that a customer has been a customer of your organization.</span></span>
- <span data-ttu-id="3e16b-112">**Aktivní od** – Toto hodnocení představuje počet let, po které odběratel podniká.</span><span class="sxs-lookup"><span data-stu-id="3e16b-112">**In business since** – This score is the number of years that a customer has been in business.</span></span> <span data-ttu-id="3e16b-113">Používá hodnotu pole **Začátek podnikání** na stránce **Odběratelé**.</span><span class="sxs-lookup"><span data-stu-id="3e16b-113">It uses the value of the **Business start** field on the **Customers** page.</span></span>
- <span data-ttu-id="3e16b-114">**Počet dnů neuhrazeného prodeje** – Toto hodnocení je založeno na zůstatku pohledávek, prodejích, výnosech a počtu dnů za předchozí dvanáctiměsíční období.</span><span class="sxs-lookup"><span data-stu-id="3e16b-114">**Days sales outstanding** – This score is based on the accounts receivable balance, sales revenue, and number of days for the previous 12-month period.</span></span>
- <span data-ttu-id="3e16b-115">**Průměrný zůstatek** – Toto hodnocení je založeno na zůstatku pohledávek za předchozí dvanáctiměsíční období.</span><span class="sxs-lookup"><span data-stu-id="3e16b-115">**Average balance** – This score is based on the accounts receivable balance for the previous 12-month period.</span></span>
- <span data-ttu-id="3e16b-116">**Skupina správy úvěru**, **Stav účtu** a **Země** – Tato hodnocení používají informace od odběratele.</span><span class="sxs-lookup"><span data-stu-id="3e16b-116">**Credit management group**, **Account status**, and **Country** – These scores use information from the customer.</span></span>

## <a name="update-customer-balance-statistics"></a><span data-ttu-id="3e16b-117">Aktualizace statistiky zůstatku odběratele</span><span class="sxs-lookup"><span data-stu-id="3e16b-117">Update customer balance statistics</span></span>

<span data-ttu-id="3e16b-118">Chcete-li aktualizovat výpočet statistiky zůstatku, která se zobrazuje na stránce **Dotaz statistiky zůstatku**, můžete spustit proces **Aktualizace statistiky zůstatku odběratele**, který aktualizuje výpočet statistiky zůstatku, jež se zobrazuje na stránce.</span><span class="sxs-lookup"><span data-stu-id="3e16b-118">You can run the **Update customer balance statistics** process to update the calculation of balance statistics that is shown on the **Balance statistics inquiry** page.</span></span> <span data-ttu-id="3e16b-119">Tyto informace se používají k výpočtu hodnocení rizik a hodnot, které se zobrazují v okně s fakty statistiky úvěru na stránce **Odběratel**.</span><span class="sxs-lookup"><span data-stu-id="3e16b-119">This information is used to calculate risk scores and the values that are shown in the credit statistics FactBoxes on the **Customer** page.</span></span>

<span data-ttu-id="3e16b-120">Při spuštění tohoto procesu se aktualizují statistiky zůstatku odběratele u jednoho odběratele.</span><span class="sxs-lookup"><span data-stu-id="3e16b-120">When you run the process, it updates customer balance statistics for a single customer.</span></span> <span data-ttu-id="3e16b-121">Chcete-li nastavit dávkovou úlohu pro spuštění procesu u více odběratelů, můžete použít stránku **Výpočet statistiky zůstatku** (**Správa úvěru \> Pravidelné úlohy \> Výpočet statistiky zůstatku**).</span><span class="sxs-lookup"><span data-stu-id="3e16b-121">To set up a batch job to run the process for multiple customers, you can use the **Calculate balance statistics** page (**Credit management \> Periodic tasks \> Calculate balance statistics**).</span></span>
