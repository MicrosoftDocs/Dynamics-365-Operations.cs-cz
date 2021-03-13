---
title: Generovat frekvenci prověřování z
description: Toto téma popisuje stav nastavený pro možnost generování četnosti prověřování Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f291e28584dadc465092d99a1354fda793ff7560
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126139"
---
# <a name="screening-frequency-generate-from"></a><span data-ttu-id="8abfe-103">Generovat frekvenci prověřování z</span><span class="sxs-lookup"><span data-stu-id="8abfe-103">Screening frequency generate from</span></span>

<span data-ttu-id="8abfe-104">Toto téma popisuje stav nastavený pro možnost generování četnosti prověřování Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8abfe-104">This topic describes the Screening frequency generate from option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="8abfe-105">Fyzický název: mshr_hcmfrequencygeneratefrom</span><span class="sxs-lookup"><span data-stu-id="8abfe-105">Physical name: mshr_hcmfrequencygeneratefrom</span></span>

<span data-ttu-id="8abfe-106">Tento výčet poskytuje sadu možností hodnot pro určení data zahájení výpočtu pro další požadovaný screening.</span><span class="sxs-lookup"><span data-stu-id="8abfe-106">This enumeration provides the option set of values for determining the start date of the calculation for the next required screening.</span></span>

| <span data-ttu-id="8abfe-107">Hodnota</span><span class="sxs-lookup"><span data-stu-id="8abfe-107">Value</span></span> | <span data-ttu-id="8abfe-108">Štítek</span><span class="sxs-lookup"><span data-stu-id="8abfe-108">Label</span></span> | <span data-ttu-id="8abfe-109">popis</span><span class="sxs-lookup"><span data-stu-id="8abfe-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="8abfe-110">200000000 Nevybráno</span><span class="sxs-lookup"><span data-stu-id="8abfe-110">200000000 Not selected</span></span> | <span data-ttu-id="8abfe-111">Nebyla vybrána žádná hodnota.</span><span class="sxs-lookup"><span data-stu-id="8abfe-111">No value has been selected.</span></span> |
| <span data-ttu-id="8abfe-112">200000001 Datum dokončení</span><span class="sxs-lookup"><span data-stu-id="8abfe-112">200000001 Date completed</span></span> | <span data-ttu-id="8abfe-113">Výpočet se provádí od posledního dokončeného data prověření.</span><span class="sxs-lookup"><span data-stu-id="8abfe-113">Calculation is done from the last screening date completed.</span></span> |
| <span data-ttu-id="8abfe-114">200000002 Datum je povinné</span><span class="sxs-lookup"><span data-stu-id="8abfe-114">200000002 Date required</span></span> | <span data-ttu-id="8abfe-115">Výpočet se provádí od posledního požadovaného data prověření.</span><span class="sxs-lookup"><span data-stu-id="8abfe-115">Calculation is done from the last screening date required.</span></span> |

## <a name="see-also"></a><span data-ttu-id="8abfe-116">Viz také</span><span class="sxs-lookup"><span data-stu-id="8abfe-116">See also</span></span>

[<span data-ttu-id="8abfe-117">Úvod do rozhraní API pro integraci systému sledování žadatelů</span><span class="sxs-lookup"><span data-stu-id="8abfe-117">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="8abfe-118">Příklad dotazu pro entitu Kandidát k přijetí</span><span class="sxs-lookup"><span data-stu-id="8abfe-118">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
