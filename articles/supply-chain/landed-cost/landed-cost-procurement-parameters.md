---
title: Parametry zásobování a získávání zdrojů pro Náklady za doručení
description: Toto téma popisuje, jak nastavit příslušné parametry zásobování a zdrojů, když používáte modul Náklady za doručení.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SrmParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: ccda3bd769a646e2390711883b8e40bec50e4d6a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020976"
---
# <a name="procurement-and-sourcing-parameters-for-landed-cost"></a><span data-ttu-id="b0abd-103">Parametry zásobování a získávání zdrojů pro Náklady za doručení</span><span class="sxs-lookup"><span data-stu-id="b0abd-103">Procurement and sourcing parameters for Landed cost</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b0abd-104">Stránka **Parametry modulu Zásobování a zdroje** obsahuje několik nastavení, která jsou zvláště důležitá, když používáte modul **Náklady za doručení**.</span><span class="sxs-lookup"><span data-stu-id="b0abd-104">The **Procurement and sourcing parameters** page has a few settings that are especially relevant when you use the **Landed cost** module.</span></span> <span data-ttu-id="b0abd-105">V dialogovém okně **Aktualizovat řádky objednávky**, které se otevírá ze stránky **Parametry modulu Zásobování a zdroje**, určete, zda mají být řádky nákupní objednávky automaticky aktualizovány, když jsou provedeny změny v záhlaví nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="b0abd-105">Use the **Update order lines** dialog box that is opened from the **Procurement and sourcing parameters** page to specify whether purchase order lines should automatically be updated when changes are made on the purchase order header.</span></span>

<span data-ttu-id="b0abd-106">Abyste dokončili toto nastavení, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="b0abd-106">To complete this setup, follow these steps.</span></span>

1. <span data-ttu-id="b0abd-107">Přejděte na **Zásobování a zdroje \> Nastavení \> Parametry modulu Zásobování a zdroje**.</span><span class="sxs-lookup"><span data-stu-id="b0abd-107">Go to **Procurement and sourcing \> Setup \> Procurement and sourcing parameters**.</span></span>
1. <span data-ttu-id="b0abd-108">Na kartě **Obecné** vyberte odkaz **Aktualizovat řádky objednávky**.</span><span class="sxs-lookup"><span data-stu-id="b0abd-108">On the **General** tab, select the **Update order lines** link.</span></span>
1. <span data-ttu-id="b0abd-109">Dialogové okno **Aktualizovat řádky objednávky** obsahuje seznam polí v záhlaví objednávky, která mohou také použít automatické aktualizace na související pole v řádcích objednávky.</span><span class="sxs-lookup"><span data-stu-id="b0abd-109">The **Update order lines** dialog box lists the fields on the order header that can also apply automatic updates to related fields on the order lines.</span></span> <span data-ttu-id="b0abd-110">Nastavte každé pole v seznamu na jednu z následujících hodnot:</span><span class="sxs-lookup"><span data-stu-id="b0abd-110">Set each field in the list to one of the following values:</span></span>

    - <span data-ttu-id="b0abd-111">**Vždy** – Řádky objednávky se aktualizují automaticky při aktualizaci záhlaví objednávky.</span><span class="sxs-lookup"><span data-stu-id="b0abd-111">**Always** – The order lines should automatically be updated when the order header is updated.</span></span>
    - <span data-ttu-id="b0abd-112">**Nikdy** – Řádky objednávky se nikdy neaktualizují při aktualizaci záhlaví objednávky.</span><span class="sxs-lookup"><span data-stu-id="b0abd-112">**Never** – The order lines should never be updated when the order header is updated.</span></span>
    - <span data-ttu-id="b0abd-113">**Výzva** - Uživatel bude vyzván k výběru, zda mají být řádky objednávky aktualizovány.</span><span class="sxs-lookup"><span data-stu-id="b0abd-113">**Prompt** – The user will be prompted to select whether the order lines should be updated.</span></span>
