---
title: Zobrazení nákladů na vyráběnou položku
description: Konstantní náklady na vyráběnou položku reflektují doby nastavení operace a komponent s konstantní kvalitou nebo s konstantní odpadovostí.
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 274483
ms.assetid: 6f5b851b-c5a7-43ef-b380-0d316667c1ef
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: b8fcfc1a9386d05c2adbcb4208e7ef5d01644430
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562246"
---
# <a name="display-charges-for-a-manufactured-item"></a><span data-ttu-id="5aebd-103">Zobrazení nákladů na vyráběnou položku</span><span class="sxs-lookup"><span data-stu-id="5aebd-103">Display charges for a manufactured item</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5aebd-104">Konstantní náklady na vyráběnou položku reflektují doby nastavení operace a komponent s konstantní kvalitou nebo s konstantní odpadovostí.</span><span class="sxs-lookup"><span data-stu-id="5aebd-104">The constant costs of a manufactured item reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span>

<span data-ttu-id="5aebd-105">Vypočtená částka nákladů na zboží může být zobrazena s náklady na jednotku zboží.</span><span class="sxs-lookup"><span data-stu-id="5aebd-105">The calculated amount of an item's charges can be displayed with the item's unit costs.</span></span> <span data-ttu-id="5aebd-106">Vedlejší náklady však někdy bývají zobrazeny jako dvě samostatná pole a nejsou zahrnuty do jednotkových nákladů na zboží.</span><span class="sxs-lookup"><span data-stu-id="5aebd-106">However, the charges are sometimes displayed as separate fields, and they are not included in the item's unit costs.</span></span> <span data-ttu-id="5aebd-107">Pokud se poplatky zobrazují s použitím samostatných polí, bude v jednom poli zobrazena celková částka nákladů a ve druhém poli bude zobrazena velikost šarže nákladů (označená jako cenová jednotka), která byla použita pro amortizaci částky.</span><span class="sxs-lookup"><span data-stu-id="5aebd-107">When the charges appear as separate fields, one field displays the total amount of charges, and another field displays the costing lot size that is used to amortize the amount.</span></span> <span data-ttu-id="5aebd-108">Na stránce Cena zboží se například náklady zobrazují jako dvě samostatná pole.</span><span class="sxs-lookup"><span data-stu-id="5aebd-108">The Item price page, for example, displays the charges as two separate fields.</span></span> <span data-ttu-id="5aebd-109">Na stránce Dokončené se však zobrazují celkové náklady na zboží podle jednotky a amortizované náklady jsou zahrnuty do jednotkových nákladů.</span><span class="sxs-lookup"><span data-stu-id="5aebd-109">However, the Complete page displays the item's total cost per unit, and the amortized costs are included in the unit costs.</span></span>

<span data-ttu-id="5aebd-110">Náklady pro vyráběnou položku jsou vždy zahrnuty do jednotkových nákladů dané položky pro účely standardních nákladů.</span><span class="sxs-lookup"><span data-stu-id="5aebd-110">The charges for a manufactured item are always included in the item's unit cost for standard cost purposes.</span></span> <span data-ttu-id="5aebd-111">Mohou být volitelně zahrnuty pro účely plánovaných nákladů.</span><span class="sxs-lookup"><span data-stu-id="5aebd-111">They can optionally be included for planned cost purposes.</span></span> <span data-ttu-id="5aebd-112">Zásady v rámci nákladové verze vynucují zahrnutí nákladů do nákladů na vyráběné zboží.</span><span class="sxs-lookup"><span data-stu-id="5aebd-112">A policy in the costing version enforces the inclusion of charges in the cost of a manufactured item.</span></span> <span data-ttu-id="5aebd-113">Když aktivujete záznam nákladů na zboží, budou aktualizovány náklady s použitím údajů o základních nákladech, které se zobrazují na stránce Cena zboží.</span><span class="sxs-lookup"><span data-stu-id="5aebd-113">When you activate an item's cost record, you update the charges for the item's base cost information, which is displayed in the Item price page.</span></span> <span data-ttu-id="5aebd-114">Vedlejší náklady jsou zobrazeny jako dvě samostatná pole a nejsou zahrnuty do jednotkových nákladů na zboží.</span><span class="sxs-lookup"><span data-stu-id="5aebd-114">The charges are displayed as two separate fields, and they are not included in the item's unit cost.</span></span> <span data-ttu-id="5aebd-115">Při každé aktivaci jsou aktualizovány údaje o základních nákladech na zboží, a to i tehdy, pokud aktivace odpovídá různým pracovištím.</span><span class="sxs-lookup"><span data-stu-id="5aebd-115">Each activation updates the item's base cost information, even if the activation reflects different sites.</span></span> <span data-ttu-id="5aebd-116">Z tohoto důvodu byste měli považovat informace o základních nákladech za referenční informace.</span><span class="sxs-lookup"><span data-stu-id="5aebd-116">Therefore, you should view the base cost information as reference information.</span></span>





