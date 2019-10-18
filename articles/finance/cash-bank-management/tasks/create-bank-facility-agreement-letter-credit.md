---
title: Vytvoření smlouvy bankovního zařízení pro akreditiv
description: Tato úloha vás provede vytvářením smlouvy bankovního zařízení pro zpracování akreditiv.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankDocumentFacilityAgreement, BankAccountTableLookUp, BankDocumentFacilityAgreementExtension, DefaultDashboard
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e63e0ffa4ddafd38595d7e9d84ffa2399a9f67b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188204"
---
# <a name="create-a-bank-facility-agreement-for-a-letter-of-credit"></a><span data-ttu-id="37835-103">Vytvoření smlouvy bankovního zařízení pro akreditiv</span><span class="sxs-lookup"><span data-stu-id="37835-103">Create a bank facility agreement for a letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="37835-104">Tato úloha vás provede vytvářením smlouvy bankovního zařízení pro zpracování akreditiv.</span><span class="sxs-lookup"><span data-stu-id="37835-104">This task walks through the creating a Bank facility agreement to process a Letter of credit.</span></span> <span data-ttu-id="37835-105">Před tímto úkolem můžete nastavit bankovní zařízení a profily zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="37835-105">You will want to set up bank facilities and posting profiles before this task.</span></span>  <span data-ttu-id="37835-106">Tento úkol využívá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="37835-106">This task uses the demo company 'USMF'.</span></span>  


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="37835-107">Vytvoření smlouvy o bankovních zařízeních</span><span class="sxs-lookup"><span data-stu-id="37835-107">Create Bank facility agreement</span></span>
1. <span data-ttu-id="37835-108">Přejděte do nabídky Pokladna a banka > Akreditivy > Smlouvy bankovního zařízení.</span><span class="sxs-lookup"><span data-stu-id="37835-108">Go to Cash and bank management > Letters of credit > Bank facility agreements.</span></span>
2. <span data-ttu-id="37835-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="37835-109">Click New.</span></span>
3. <span data-ttu-id="37835-110">Do pole Číslo smlouvy zadejte číslo smlouvy podle dohody s bankou.</span><span class="sxs-lookup"><span data-stu-id="37835-110">In the Agreement number field, enter the agreement number according to the agreement with the bank.</span></span>
4. <span data-ttu-id="37835-111">Do pole Bankovní číslo zadejte číslo účtu určené bankou.</span><span class="sxs-lookup"><span data-stu-id="37835-111">In the Bank account field, enter the account number at the issuing bank.</span></span>
5. <span data-ttu-id="37835-112">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="37835-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="37835-113">Do pole Počáteční datum zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="37835-113">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="37835-114">Do pole Konečné datum zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="37835-114">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="37835-115">Rozbalte nebo sbalte oddíl Obecné.</span><span class="sxs-lookup"><span data-stu-id="37835-115">Expand or collapse the General section.</span></span>
9. <span data-ttu-id="37835-116">Klikněte na Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="37835-116">Click Add line.</span></span>
10. <span data-ttu-id="37835-117">V poli Typ zařízení kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="37835-117">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="37835-118">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="37835-118">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="37835-119">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="37835-119">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="37835-120">V poli Limit zadejte objem zařízení sjednaný s bankou.</span><span class="sxs-lookup"><span data-stu-id="37835-120">In the Limit field, enter the facility amount that was negotiated with the bank.</span></span>
14. <span data-ttu-id="37835-121">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="37835-121">Click Save.</span></span>
15. <span data-ttu-id="37835-122">Kliknutím na možnost Rozšířit otevřete dialog Zanechat.</span><span class="sxs-lookup"><span data-stu-id="37835-122">Click Extend to open the drop dialog.</span></span>
16. <span data-ttu-id="37835-123">Zadejte hodnotu do pole Nové číslo smlouvy.</span><span class="sxs-lookup"><span data-stu-id="37835-123">In the New agreement number field, type a value.</span></span>
17. <span data-ttu-id="37835-124">Do pole Konečné datum zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="37835-124">In the End date field, enter a date and time.</span></span>
18. <span data-ttu-id="37835-125">Klepněte na položku Rozšířit.</span><span class="sxs-lookup"><span data-stu-id="37835-125">Click Extend.</span></span>
19. <span data-ttu-id="37835-126">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="37835-126">Close the page.</span></span>

