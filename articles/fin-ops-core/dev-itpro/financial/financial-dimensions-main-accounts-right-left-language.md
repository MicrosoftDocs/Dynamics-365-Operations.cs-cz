---
title: Finanční dimenze a hlavní účty v jazycích s psaním zprava doleva
description: Toto téma popisuje rozhodnutí, která je třeba zvážit, pokud používáte jazyk psaný zprava doleva a potřebujete nastavit finanční dimenze a hlavní účty.
author: RyanCCarlson2
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: rhaertle
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: rcarlson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 26fd186415db0adf01b8c53b188171fcf86fbc88
ms.sourcegitcommit: eff3da7ea98758f100d44ff7feec17157afc2e80
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/27/2021
ms.locfileid: "6111655"
---
# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a><span data-ttu-id="10bb8-103">Finanční dimenze a hlavní účty v jazycích s psaním zprava doleva</span><span class="sxs-lookup"><span data-stu-id="10bb8-103">Financial dimensions and main accounts in right-to-left languages</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="10bb8-104">Toto téma popisuje některá implementační rozhodnutí, která byste měli zvážit, pokud používáte jazyk psaný zprava doleva a potřebujete nastavit finanční dimenze a hlavní účty.</span><span class="sxs-lookup"><span data-stu-id="10bb8-104">This topic describes some of the implementation decisions that you should consider when you use a right-to-left language, and you must set up financial dimensions and main accounts.</span></span>

<span data-ttu-id="10bb8-105">Finanční dimenze a hlavní účty jsou klíčové součásti fázi plánování pro implementaci.</span><span class="sxs-lookup"><span data-stu-id="10bb8-105">Financial dimensions and main accounts are key components of the planning phase for an implementation.</span></span> <span data-ttu-id="10bb8-106">Po vytvoření se finanční dimenze a hlavní účty v systému používají na stránkách **Konfigurování účetní struktury**, **Rozšířené struktury pravidel** a **konfigurace finanční dimenze pro integraci aplikací**.</span><span class="sxs-lookup"><span data-stu-id="10bb8-106">After financial dimensions and main accounts are created in the system, they are used on the **Configure account structures**, **Advanced rule structures**, and **Financial dimension configuration for integrating applications** pages.</span></span> <span data-ttu-id="10bb8-107">Pořadí, které je definováno na těchto stránkách, slouží v systému k zadávání dat a spotřeby.</span><span class="sxs-lookup"><span data-stu-id="10bb8-107">The order that is defined on those pages is used in the system for data entry and consumption.</span></span> <span data-ttu-id="10bb8-108">V některých místech v systému se finanční dimenze a hlavní účty zobrazují v samostatných polích.</span><span class="sxs-lookup"><span data-stu-id="10bb8-108">In some places in the system, the financial dimensions and main accounts appear in separate fields.</span></span> <span data-ttu-id="10bb8-109">Na dalších místech, jako jsou například deníky, finanční dimenze a hlavní účty, se zobrazí jako jeden řetězec.</span><span class="sxs-lookup"><span data-stu-id="10bb8-109">In other places, such as journals, the financial dimensions and main accounts appear as a single string.</span></span>

## <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a><span data-ttu-id="10bb8-110">Doporučené postupy při nastavování finančních dimenzí a hlavních účtů v systému zprava doleva</span><span class="sxs-lookup"><span data-stu-id="10bb8-110">Best practices for setting up financial dimensions and main accounts in a right-to-left system</span></span>

- <span data-ttu-id="10bb8-111">Vyberete-li oddělovač účtové osnovy, vyberte jednu z možností dvojího oddělovače: dvojitá pomlčka (`--`), dvě čáry (`||`), dvě tečky (`..`), nebo dvojnásobné podtržení (`\\`).</span><span class="sxs-lookup"><span data-stu-id="10bb8-111">When you select the delimiter for charts of accounts, select one of the double delimiter options: double hyphen (`--`), double bar (`||`), double period (`..`), or double underscore (`\\`).</span></span>
- <span data-ttu-id="10bb8-112">Když vytvoříte finanční dimenzi a hodnoty hlavního účtu, použijte pouze číslice a znaky zprava doleva.</span><span class="sxs-lookup"><span data-stu-id="10bb8-112">When you create financial dimension and main account values, use only numbers and right-to-left language characters.</span></span>
- <span data-ttu-id="10bb8-113">Nepoužívejte vybrané oddělovače účtové osnovy ve finanční dimenzi a hodnotách hlavního účtu.</span><span class="sxs-lookup"><span data-stu-id="10bb8-113">Avoid using the selected chart of accounts delimiter in financial dimension and main account values.</span></span>

<span data-ttu-id="10bb8-114">Podle těchto doporučených postupů můžete zajistit konzistentní reprezentaci uživatelem definované objednávky v celém systému.</span><span class="sxs-lookup"><span data-stu-id="10bb8-114">By following these best practices, you help guarantee consistent representation of the user defined-order throughout the system.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]