---
title: Nesprávná hodnota pole v záznamu TaxTrans
description: Toto téma poskytuje informace o řešení potíží s nesprávnými hodnotami polí v záznamu TaxTrans.
author: bijian
manager: beya
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 97f9bb24d32180f2fccb69c5a13e2aa0349c1ee4
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947606"
---
# <a name="incorrect-field-value-in-taxtrans"></a><span data-ttu-id="2dc7c-103">Nesprávná hodnota pole v záznamu TaxTrans</span><span class="sxs-lookup"><span data-stu-id="2dc7c-103">Incorrect field value in TaxTrans</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2dc7c-104">Pokud je hodnota pole v záznamu **TaxTrans** nesprávná, pokuste se problém vyřešit pomocí informací v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="2dc7c-104">If a field value in **TaxTrans** is incorrect, use the information in this topic to try to resolve the issue.</span></span>

## <a name="overview-of-values"></a><span data-ttu-id="2dc7c-105">Přehled hodnot</span><span class="sxs-lookup"><span data-stu-id="2dc7c-105">Overview of values</span></span>
<span data-ttu-id="2dc7c-106">Následující seznam ukazuje, jak jsou záznamy **TaxTrans**, **TaxUncommitted** a **TmpTaxWorkTrans** podobné datové sady, ale fungují odlišně.</span><span class="sxs-lookup"><span data-stu-id="2dc7c-106">The following list shows how **TaxTrans**, **TaxUncommitted**, and **TmpTaxWorkTrans** are similar data sets, but in work differently.</span></span>

  - <span data-ttu-id="2dc7c-107">**TaxTrans** je konečný výsledek zaúčtované daňové transakce přetrvávající v databázi.</span><span class="sxs-lookup"><span data-stu-id="2dc7c-107">**TaxTrans** is the final posted tax transaction result persisted in the database.</span></span>
  - <span data-ttu-id="2dc7c-108">**TaxUncommitted** je přechodný vypočítaný daňový výsledek přetrvávající v databázi (pokud existuje), který bude použit později při účtování.</span><span class="sxs-lookup"><span data-stu-id="2dc7c-108">**TaxUncommitted** is the intermediate calculated tax result persisted in the database (if applicable), which will be used later in posting.</span></span>
  - <span data-ttu-id="2dc7c-109">**TmpTaxWorkTrans** je dočasný vypočítaný výsledek daně v tabulce v paměti (typ tabulky = InMemory).</span><span class="sxs-lookup"><span data-stu-id="2dc7c-109">**TmpTaxWorkTrans** is the temporary calculated tax result in the in-memory table (Table Type = InMemory).</span></span>

<span data-ttu-id="2dc7c-110">Pokud zjistíte hlavní příčinu nesprávnosti sloupce **TaxTrans**, zjistili jste také hlavní příčinu nesprávnosti sloupců **TaxUncommitted** nebo **TmpTaxWorkTrans**.</span><span class="sxs-lookup"><span data-stu-id="2dc7c-110">If you find the root cause of an incorrect **TaxTrans** column, you've also found the root cause of an incorrect **TaxUncommitted** or **TmpTaxWorkTrans** column.</span></span> <span data-ttu-id="2dc7c-111">Je to proto, že tyto tři sloupce jsou navzájem kopírovány.</span><span class="sxs-lookup"><span data-stu-id="2dc7c-111">This is because the three columns are copied from each other.</span></span>

<span data-ttu-id="2dc7c-112">Během výpočtu daně se obvykle generuje záznam **TmpTaxWorkTrans** a poté, pokud je to relevantní, se generuje záznam **TaxUncommitted**.</span><span class="sxs-lookup"><span data-stu-id="2dc7c-112">Typically, during tax calculation, **TmpTaxWorkTrans** is generated, and then, if applicable, **TaxUncommitted** is generated.</span></span> <span data-ttu-id="2dc7c-113">Během účtování daní se generuje záznam **TaxTrans**.</span><span class="sxs-lookup"><span data-stu-id="2dc7c-113">During tax posting, **TaxTrans** is generated.</span></span>


## <a name="add-breakpoints"></a><span data-ttu-id="2dc7c-114">Přidání zarážek</span><span class="sxs-lookup"><span data-stu-id="2dc7c-114">Add breakpoints</span></span>
<span data-ttu-id="2dc7c-115">Pomocí následujících kroků přidáte zarážky:</span><span class="sxs-lookup"><span data-stu-id="2dc7c-115">To add breakpoints, complete the following steps:</span></span> 

1. <span data-ttu-id="2dc7c-116">Přidejte rozšíření a zarážky do příkazů *insert()* a *update()* v rozšířeních, jak je znázorněno níže.</span><span class="sxs-lookup"><span data-stu-id="2dc7c-116">Add extensions and breakpoints in *insert()* and *update()* in the extensions as shown below.</span></span>

     - <span data-ttu-id="2dc7c-117">**TaxTrans**</span><span class="sxs-lookup"><span data-stu-id="2dc7c-117">**TaxTrans**</span></span>

        ```x++
        [ExtensionOf(tableStr(TaxTrans))]
        public final class TaxTrans_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - <span data-ttu-id="2dc7c-118">**TaxUncommitted**</span><span class="sxs-lookup"><span data-stu-id="2dc7c-118">**TaxUncommitted**</span></span>

        ```x++
        [ExtensionOf(tableStr(TaxUncommitted))]
        public final class TaxUncommitted_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - <span data-ttu-id="2dc7c-119">**TmpTaxWorkTrans**</span><span class="sxs-lookup"><span data-stu-id="2dc7c-119">**TmpTaxWorkTrans**</span></span>

        ```x++
        [ExtensionOf(tableStr(TmpTaxWorkTrans))]
        public final class TmpTaxWorkTrans_Extension
        {
            public void insert(boolean _ignoreCalculatedSalesTax)
            {
                next insert(_ignoreCalculatedSalesTax);
            }
        
            public void update(boolean _ignoreCalculatedSalesTax)
            {
                next update(_ignoreCalculatedSalesTax);
            }
        
        }
        
        ```

2. <span data-ttu-id="2dc7c-120">Alternativně můžete přidat zarážky přímo, když není zahrnut záznam **TaxUncommitted**.</span><span class="sxs-lookup"><span data-stu-id="2dc7c-120">Alternatively, you can add breakpoints directly when **TaxUncommitted** is not included.</span></span>

     - <span data-ttu-id="2dc7c-121">*TaxTrans.insert()*, *TaxTrans.update()*</span><span class="sxs-lookup"><span data-stu-id="2dc7c-121">*TaxTrans.insert()*, *TaxTrans.update()*</span></span>
     - <span data-ttu-id="2dc7c-122">*TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*</span><span class="sxs-lookup"><span data-stu-id="2dc7c-122">*TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*</span></span>

## <a name="reproduce-and-debug"></a><span data-ttu-id="2dc7c-123">Reprodukce a ladění</span><span class="sxs-lookup"><span data-stu-id="2dc7c-123">Reproduce and debug</span></span>

<span data-ttu-id="2dc7c-124">Po nastavení zarážek je každá změna perzistence dat viditelná během ladění.</span><span class="sxs-lookup"><span data-stu-id="2dc7c-124">After the breakpoints are set, every data persistency change is visible during debugging.</span></span> <span data-ttu-id="2dc7c-125">Chcete-li najít hlavní příčinu nesprávného sloupce **TaxTrans**, **TaxUncommitted** nebo **TmpTaxWorkTrans**, zkontrolujte a poznamenejte si následující položky:</span><span class="sxs-lookup"><span data-stu-id="2dc7c-125">To find the root cause of an incorrect column of **TaxTrans**, **TaxUncommitted**, or **TmpTaxWorkTrans**, review and note the following items:</span></span>

- <span data-ttu-id="2dc7c-126">Poslední zarážka, kde je sloupec správný.</span><span class="sxs-lookup"><span data-stu-id="2dc7c-126">The last breakpoint where the column is correct.</span></span>
- <span data-ttu-id="2dc7c-127">První zarážka, kde je sloupec nesprávný.</span><span class="sxs-lookup"><span data-stu-id="2dc7c-127">The first breakpoint where the column is incorrect.</span></span>
- <span data-ttu-id="2dc7c-128">Co se děje mezi těmito dvěma body.</span><span class="sxs-lookup"><span data-stu-id="2dc7c-128">What happens in between those two points.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="2dc7c-129">Zjištění, zda existuje přizpůsobení</span><span class="sxs-lookup"><span data-stu-id="2dc7c-129">Determine whether customization exists</span></span>
<span data-ttu-id="2dc7c-130">Pokud jste dokončili kroky v předchozích částech, ale problém se vám nepodařilo vyřešit, zjistěte, zda existuje přizpůsobení.</span><span class="sxs-lookup"><span data-stu-id="2dc7c-130">If you've completed the steps in the previous sections but have not been able to resolve the issue, determine whether customization exists.</span></span> <span data-ttu-id="2dc7c-131">Pokud žádné přizpůsobení neexistuje, požádejte o pomoc podporu společnosti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2dc7c-131">If no customization exists, contact Microsoft Support for assistance.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

