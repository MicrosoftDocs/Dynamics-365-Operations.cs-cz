---
title: Úvěrové skupiny odběratele
description: Toto téma obsahuje informace o skupinách odběratelů podle limitu úvěru.
author: mikefalkner
manager: AnnBe
ms.date: 04/14/2020
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
ms.openlocfilehash: 90d75493b928bfa4edafeef7730bc272c9146192
ms.sourcegitcommit: cd8a28be0acf31c547db1b8f6703dd4b0f62940c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261250"
---
# <a name="customer-credit-groups"></a><span data-ttu-id="b1e18-103">Úvěrové skupiny zákazníka</span><span class="sxs-lookup"><span data-stu-id="b1e18-103">Customer credit groups</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1e18-104">Můžete definovat skupiny odběratelů, kteří mají sdílený limit úvěru.</span><span class="sxs-lookup"><span data-stu-id="b1e18-104">You can define groups of customers who have a shared credit limit.</span></span> <span data-ttu-id="b1e18-105">Zohledňuje se také individuální limit úvěru, který je definovaný v účtu faktury odběratele.</span><span class="sxs-lookup"><span data-stu-id="b1e18-105">The individual credit limit that is defined on the customer invoice account is also considered.</span></span>

<span data-ttu-id="b1e18-106">Členy skupiny odběratelů podle limitu úvěru lze vybírat z různých právnických osob.</span><span class="sxs-lookup"><span data-stu-id="b1e18-106">Members of a customer credit group can be selected from different legal entities.</span></span> <span data-ttu-id="b1e18-107">Přidáte-li odběratele do seznamu odběratelů ve skupině odběratelů podle limitu úvěru, datum vypršení platnosti limitu úvěru pro každého odběratele se změní na datum vypršení platnosti přiřazené ke skupině.</span><span class="sxs-lookup"><span data-stu-id="b1e18-107">When you add a customer to the list of customers in the customer credit group, the expiration date of the credit limit for each customer is changed to the expiration date that is assigned to the group.</span></span>

<span data-ttu-id="b1e18-108">Na stránce **Skupiny odběratelů podle limitu úvěru** (**Správa úvěru \> Skupiny odběratelů podle limitu úvěru \> Skupiny odběratelů podle limitu úvěru**) můžete nastavit skupiny odběratelů podle limitu úvěru.</span><span class="sxs-lookup"><span data-stu-id="b1e18-108">You can set up customer credit groups on the **Customer credit groups** page (**Credit management \> Customer credit groups \> Customer credit groups**).</span></span>

1. <span data-ttu-id="b1e18-109">Do polí **Číslo skupiny** a **Popis** zadejte identifikátor a popis skupiny.</span><span class="sxs-lookup"><span data-stu-id="b1e18-109">In the **Group number** and **Description** fields, enter an identifier and description for the group.</span></span>
2. <span data-ttu-id="b1e18-110">Do polí **Limit úvěru** a **Měna** zadejte limit úvěru a měnu, které mají být použity v případě, že systém kontroluje limit úvěru pro libovolného člena skupiny.</span><span class="sxs-lookup"><span data-stu-id="b1e18-110">In the **Credit limit** and **Currency** fields, enter the credit limit and currency that should be used when the system checks the credit limit for any member of the group.</span></span>
3. <span data-ttu-id="b1e18-111">Do pole **Konečné datum limitu úvěru** zadejte datum vypršení platnosti limitu úvěru.</span><span class="sxs-lookup"><span data-stu-id="b1e18-111">In the **Credit limit to date** field, enter the date when the credit limit expires.</span></span> <span data-ttu-id="b1e18-112">Skupiny odběratelů podle limitu úvěru musí mít stanoveno datum vypršení platnosti.</span><span class="sxs-lookup"><span data-stu-id="b1e18-112">Customer credit groups must have an expiration date.</span></span>

<span data-ttu-id="b1e18-113">Po dokončení nastavení skupiny odběratelů podle limitu úvěru můžete do skupiny přidat odběratele zadáním jejich právnické osoby a ID účtu odběratele.</span><span class="sxs-lookup"><span data-stu-id="b1e18-113">After you've finished setting up a customer credit group, you can add customers to it by specifying their legal entity and customer account ID.</span></span> <span data-ttu-id="b1e18-114">Když přidáte nového odběratele do skupiny odběratelů podle limitu úvěru, systém vyhledá stejný účet odběratele v rámci všech právnických osob a vyzve vás k jeho přidání do skupiny odběratelů podle limitu úvěru.</span><span class="sxs-lookup"><span data-stu-id="b1e18-114">When you add a new customer to a customer credit group, the system searches for the same customer account across all legal entities and prompts you to add it to the customer credit group.</span></span>

<span data-ttu-id="b1e18-115">Nabídka **Splatné zůstatky** slouží k zobrazení podrobností o splatném zůstatku pro všechny odběratele na faktuře ve skupině odběratelů podle limitu úvěru.</span><span class="sxs-lookup"><span data-stu-id="b1e18-115">Use the **Aged balances** menu to view the details of the aging balance for all invoice customers in a customer credit group.</span></span> <span data-ttu-id="b1e18-116">Na stránce **Splatný zůstatek** se zobrazuje souhrn splatných zůstatků pro účty odběratelů na fakturách.</span><span class="sxs-lookup"><span data-stu-id="b1e18-116">The **Aging balance** page shows a summary of the aged balances for the invoice customer accounts.</span></span>
