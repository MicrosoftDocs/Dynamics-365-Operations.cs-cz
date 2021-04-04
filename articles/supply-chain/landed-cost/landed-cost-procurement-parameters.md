---
title: Parametry zásobování a získávání zdrojů pro Náklady za doručení
description: Toto téma popisuje, jak nastavit příslušné parametry zásobování a zdrojů, když používáte modul Náklady za doručení.
author: sherry-zheng
manager: tfehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 49e046a1437917cfa866f690511789496fac2c53
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500735"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a><span data-ttu-id="f19e6-103">Parametry zásobování a získávání zdrojů pro Náklady za doručení</span><span class="sxs-lookup"><span data-stu-id="f19e6-103">Procurement and sourcing parameters for Landed cost</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="f19e6-104">Stránka **Parametry modulu Zásobování a zdroje** obsahuje několik nastavení, která jsou zvláště důležitá, když používáte modul **Náklady za doručení**.</span><span class="sxs-lookup"><span data-stu-id="f19e6-104">The **Procurement and sourcing parameters** page has a few settings that are especially relevant when you use the **Landed cost** module.</span></span> <span data-ttu-id="f19e6-105">V dialogovém okně **Aktualizovat řádky objednávky**, které se otevírá ze stránky **Parametry modulu Zásobování a zdroje**, určete, zda mají být řádky nákupní objednávky automaticky aktualizovány, když jsou provedeny změny v záhlaví nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="f19e6-105">Use the **Update order lines** dialog box that is opened from the **Procurement and sourcing parameters** page to specify whether purchase order lines should automatically be updated when changes are made on the purchase order header.</span></span>

<span data-ttu-id="f19e6-106">Abyste dokončili toto nastavení, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="f19e6-106">To complete this setup, follow these steps.</span></span>

1. <span data-ttu-id="f19e6-107">Přejděte na **Zásobování a zdroje \> Nastavení \> Parametry modulu Zásobování a zdroje**.</span><span class="sxs-lookup"><span data-stu-id="f19e6-107">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing parameters**.</span></span>
1. <span data-ttu-id="f19e6-108">Na kartě **Obecné** vyberte odkaz **Aktualizovat řádky objednávky**.</span><span class="sxs-lookup"><span data-stu-id="f19e6-108">On the **General** tab, select the **Update order lines** link.</span></span>
1. <span data-ttu-id="f19e6-109">Dialogové okno **Aktualizovat řádky objednávky** obsahuje seznam polí v záhlaví objednávky, která mohou také použít automatické aktualizace na související pole v řádcích objednávky.</span><span class="sxs-lookup"><span data-stu-id="f19e6-109">The **Update order lines** dialog box lists the fields on the order header that can also apply automatic updates to related fields on the order lines.</span></span> <span data-ttu-id="f19e6-110">Nastavte každé pole v seznamu na jednu z následujících hodnot:</span><span class="sxs-lookup"><span data-stu-id="f19e6-110">Set each field in the list to one of the following values:</span></span>

    - <span data-ttu-id="f19e6-111">**Vždy** – Řádky objednávky se aktualizují automaticky při aktualizaci záhlaví objednávky.</span><span class="sxs-lookup"><span data-stu-id="f19e6-111">**Always** – The order lines should automatically be updated when the order header is updated.</span></span>
    - <span data-ttu-id="f19e6-112">**Nikdy** – Řádky objednávky se nikdy neaktualizují při aktualizaci záhlaví objednávky.</span><span class="sxs-lookup"><span data-stu-id="f19e6-112">**Never** – The order lines should never be updated when the order header is updated.</span></span>
    - <span data-ttu-id="f19e6-113">**Výzva** - Uživatel bude vyzván k výběru, zda mají být řádky objednávky aktualizovány.</span><span class="sxs-lookup"><span data-stu-id="f19e6-113">**Prompt** – The user will be prompted to select whether the order lines should be updated.</span></span>
