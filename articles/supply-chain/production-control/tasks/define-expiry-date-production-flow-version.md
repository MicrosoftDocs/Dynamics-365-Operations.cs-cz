---
title: Definování data vypršení platnosti verze výrobního toku
description: Pro ukončení platnosti a zpracování verze výrobního toku k danému datu nebo naplánování nahrazení aktivní verze novou verzí je nutné nastavit datum vypršení platnosti na verzi.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10260290fba02ebf9313d0d1355c9aa28e3509d7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843690"
---
# <a name="define-an-expiry-date-for-a-production-flow-version"></a><span data-ttu-id="39547-103">Definování data vypršení platnosti verze výrobního toku</span><span class="sxs-lookup"><span data-stu-id="39547-103">Define an expiry date for a production flow version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="39547-104">Pro ukončení platnosti a zpracování verze výrobního toku k danému datu nebo naplánování nahrazení aktivní verze novou verzí je nutné nastavit datum vypršení platnosti na verzi.</span><span class="sxs-lookup"><span data-stu-id="39547-104">To end the validity and the processing of a production flow version on a given date, or to plan replacement of an active version with a new version, you have to set an expiry date on the version.</span></span> <span data-ttu-id="39547-105">Není nutné deaktivovat verzi.</span><span class="sxs-lookup"><span data-stu-id="39547-105">It is not necessary to deactivate the version.</span></span>


## <a name="set-an-expiration-date-to-end-a-production-flow-version"></a><span data-ttu-id="39547-106">Nastavení data vypršení platnosti k ukončení verze výrobního toku</span><span class="sxs-lookup"><span data-stu-id="39547-106">Set an expiration date to end a production flow version</span></span>
1. <span data-ttu-id="39547-107">Přejděte na Řízení výroby > Nastavení > Tok štíhlé výroby > Výrobního toky.</span><span class="sxs-lookup"><span data-stu-id="39547-107">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="39547-108">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="39547-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="39547-109">Vyberte výrobní tok, který má verzi, která je již definována.</span><span class="sxs-lookup"><span data-stu-id="39547-109">Select any production flow that has a version that is already defined.</span></span>  
3. <span data-ttu-id="39547-110">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="39547-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="39547-111">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="39547-111">Click Edit.</span></span>
5. <span data-ttu-id="39547-112">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="39547-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="39547-113">Do pole Datum vypršení platnosti zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="39547-113">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="39547-114">Pro datum vypršení platnosti se nová verze nespustí nebo neaktivuje.</span><span class="sxs-lookup"><span data-stu-id="39547-114">For the expiration date, a new version will not start or become activated.</span></span> <span data-ttu-id="39547-115">Také již nebude možné vytvořit nebo spustit úlohy pro tento výrobní tok.</span><span class="sxs-lookup"><span data-stu-id="39547-115">It will also no longer be possible to create or start jobs for this production flow.</span></span> <span data-ttu-id="39547-116">Dále můžete dokončit zahájené úlohy po datu vypršení platnosti.</span><span class="sxs-lookup"><span data-stu-id="39547-116">You can still complete started jobs after the expiration date.</span></span>  

