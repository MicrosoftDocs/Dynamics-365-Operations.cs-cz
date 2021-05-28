---
title: Výpočet TDS u mezipodnikových transakcí
description: Toto téma popisuje proces, který se používá k výpočtu daně odečtené u zdroje (TDS) u mezipodnikových transakcí ve fázích.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 0e304747cc93bfe0a39beababc3182ca14664b11
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023091"
---
# <a name="tds-calculation-on-intercompany-transactions"></a><span data-ttu-id="ddd0e-103">Výpočet TDS u mezipodnikových transakcí</span><span class="sxs-lookup"><span data-stu-id="ddd0e-103">TDS calculation on intercompany transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ddd0e-104">Toto téma popisuje proces, který se používá k výpočtu daně odečtené u zdroje (TDS) u mezipodnikových transakcí ve fázích.</span><span class="sxs-lookup"><span data-stu-id="ddd0e-104">This topic describes the process that is used to calculate Tax Deducted at Source (TDS) on intercompany transactions in phases.</span></span>

<span data-ttu-id="ddd0e-105">Když je vytvořena mezipodniková nákupní objednávka nebo prodejní objednávka, použije se k výpočtu částky TDS výchozí skupina TDS, která je definována pro zákazníka nebo dodavatele.</span><span class="sxs-lookup"><span data-stu-id="ddd0e-105">When an intercompany purchase order or sales order is created, the default TDS group that is defined for the customer or vendor is used to calculate the TDS amount.</span></span> <span data-ttu-id="ddd0e-106">Po zaúčtování faktury se částka TDS zaúčtuje na vratné nebo splatné účty.</span><span class="sxs-lookup"><span data-stu-id="ddd0e-106">The TDS amount is posted to the recoverable or payable accounts after the invoice is posted.</span></span>

<span data-ttu-id="ddd0e-107">Mezipodniková prodejní objednávka nebo nákupní objednávka se automaticky vytvoří pro původní nákupní objednávku nebo prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="ddd0e-107">An intercompany sales order or purchase order is automatically created for the original purchase order or sales order.</span></span> <span data-ttu-id="ddd0e-108">Výchozí skupina TDS se zobrazuje na mezipodnikové objednávce, takže lze vypočítat TDS.</span><span class="sxs-lookup"><span data-stu-id="ddd0e-108">The default TDS group is shown on the intercompany order, so that TDS can be calculated.</span></span> <span data-ttu-id="ddd0e-109">Skupinu TDS můžete změnit.</span><span class="sxs-lookup"><span data-stu-id="ddd0e-109">You can change the TDS group.</span></span> <span data-ttu-id="ddd0e-110">Fakturu lze zaúčtovat pouze v případě, že čistá částka faktury na mezipodnikové objednávce, která je automaticky vytvořena, odpovídá čisté částce faktury na původní objednávce.</span><span class="sxs-lookup"><span data-stu-id="ddd0e-110">The invoice can be posted only if the net invoice amount on the intercompany order that is automatically created matches the net invoice amount on the original order.</span></span> <span data-ttu-id="ddd0e-111">(Čistá částka je částka faktury po odečtení TDS.)</span><span class="sxs-lookup"><span data-stu-id="ddd0e-111">(The net amount is the invoice amount after TDS is deducted.)</span></span>

<span data-ttu-id="ddd0e-112">Například je vytvořena prodejní faktura pro 50 000 a je k ní připojena skupina TDS **10 %**.</span><span class="sxs-lookup"><span data-stu-id="ddd0e-112">For example, a sales invoice is created for 50,000, and the **10%** TDS group is attached to it.</span></span> <span data-ttu-id="ddd0e-113">Zaúčtovaná částka faktury je 45 000 a zaúčtovaná částka TDS prodejní faktury je 5 000.</span><span class="sxs-lookup"><span data-stu-id="ddd0e-113">The posted invoice amount is 45,000, and the posted TDS amount for the sales invoice is 5,000.</span></span> <span data-ttu-id="ddd0e-114">Nákupní objednávka se automaticky vytvoří pro mezipodnikovou prodejní objednávku a je k ní připojena skupina TDS **10 %**.</span><span class="sxs-lookup"><span data-stu-id="ddd0e-114">A purchase order is automatically created for the intercompany sales order, and the  **10%** TDS group is attached to it.</span></span> <span data-ttu-id="ddd0e-115">Pokud změníte skupinu TDS na **15 %**, nemůžete zaúčtovat fakturu, protože čistá částka faktury mezipodnikové prodejní objednávky, která byla automaticky vytvořena, se neshoduje s čistou částkou faktury původní prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="ddd0e-115">If you change the TDS group to **15%**, you can't post the invoice, because the net invoice amount of the intercompany sales order that was automatically created doesn't match the net invoice amount of the original sales order.</span></span>

<span data-ttu-id="ddd0e-116">Deník plateb, který je vytvořen pro mezipodnikovou fakturu, je automaticky zaúčtován.</span><span class="sxs-lookup"><span data-stu-id="ddd0e-116">A payment journal that is created for an intercompany invoice is automatically posted.</span></span> <span data-ttu-id="ddd0e-117">Tento deník plateb lze zaúčtovat pouze v případě, že částka čisté platby v něm odpovídá částce čisté platby v původním deníku plateb.</span><span class="sxs-lookup"><span data-stu-id="ddd0e-117">That payment journal can be posted only if the net payment amount on it matches the net payment amount on the original payment journal.</span></span>
