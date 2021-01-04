---
title: Povolení výpočtu opožděné daně v denících
description: Toto téma vysvětluje, jak pomocí funkce Povolit výpočet výpočet opožděné daně v deníku zvýšit výkonnost výpočtu daně, pokud je objem řádků deníku velmi velký.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: d4ce0343ac766b30d532be0866a381dc520fd462
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441259"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a><span data-ttu-id="d568b-103">Povolení výpočtu opožděné daně v denících</span><span class="sxs-lookup"><span data-stu-id="d568b-103">Enable delayed tax calculation on journals</span></span>
[!include [banner](../includes/banner.md)]


<span data-ttu-id="d568b-104">V tomto tématu je vysvětleno, jak lze zpozdit výpočet DPH v denících.</span><span class="sxs-lookup"><span data-stu-id="d568b-104">This topic explains how you can delay sales tax calculation on journals.</span></span> <span data-ttu-id="d568b-105">Tato schopnost pomáhá zvýšit výkon při výpočtech daně v případě, že existuje mnoho řádků deníku.</span><span class="sxs-lookup"><span data-stu-id="d568b-105">This capability helps improve the performance of tax calculations when there are many journal lines.</span></span>

<span data-ttu-id="d568b-106">Ve výchozím nastavení jsou částky DPH na řádcích deníku vypočteny při aktualizaci polí vztahujících se k dani.</span><span class="sxs-lookup"><span data-stu-id="d568b-106">By default, sales tax amounts on journal lines are calculated whenever tax-related fields are updated.</span></span> <span data-ttu-id="d568b-107">Mezi tato pole patří pole pro skupiny DPH a skupiny DPH položky.</span><span class="sxs-lookup"><span data-stu-id="d568b-107">These fields include the fields for sales tax groups and item sales tax groups.</span></span> <span data-ttu-id="d568b-108">Jakákoli aktualizace řádku deníku způsobí přepočítání částek daně pro všechny řádky deníku.</span><span class="sxs-lookup"><span data-stu-id="d568b-108">Any update to a journal line causes tax amounts to be recalculated for all journal lines.</span></span> <span data-ttu-id="d568b-109">Ačkoli toto chování pomáhá uživateli zobrazit částky daně vypočtené v reálném čase, může také ovlivňovat výkonnost v případě, že je počet řádků deníku velmi velký.</span><span class="sxs-lookup"><span data-stu-id="d568b-109">Although this behavior helps user see tax amounts calculated in real time, it can also affect performance if the number of journal lines is very large.</span></span>

<span data-ttu-id="d568b-110">Funkce výpočtu opožděné daně umožňuje zpozdit výpočet daně v denících, a proto může pomoci vyřešit problémy s výkonem.</span><span class="sxs-lookup"><span data-stu-id="d568b-110">The Delayed tax calculation feature lets you delay tax calculation on journals and therefore helps fix performance issues.</span></span> <span data-ttu-id="d568b-111">Je-li tato funkce zapnuta, budou částky daně vypočteny pouze v případě, že uživatel klikne na příkaz **DPH** nebo zaúčtuje deník.</span><span class="sxs-lookup"><span data-stu-id="d568b-111">When this feature is turned on, tax amounts are calculated only when a user selects **Sales Tax** or posts the journal.</span></span>

<span data-ttu-id="d568b-112">Výpočet DPH můžete zpozdit ze tří úrovní:</span><span class="sxs-lookup"><span data-stu-id="d568b-112">You can delay the calculation of sales taxes at three levels:</span></span>

- <span data-ttu-id="d568b-113">Právnická osoba</span><span class="sxs-lookup"><span data-stu-id="d568b-113">Legal entity</span></span>
- <span data-ttu-id="d568b-114">Název deníku</span><span class="sxs-lookup"><span data-stu-id="d568b-114">Journal name</span></span>
- <span data-ttu-id="d568b-115">Záhlaví deníku</span><span class="sxs-lookup"><span data-stu-id="d568b-115">Journal header</span></span>

<span data-ttu-id="d568b-116">Systém dává prioritu nastavení pro záhlaví deníku.</span><span class="sxs-lookup"><span data-stu-id="d568b-116">The system gives priority to the setting for the journal header.</span></span> <span data-ttu-id="d568b-117">Ve výchozím nastavení je toto nastavení převzato z názvu deníku.</span><span class="sxs-lookup"><span data-stu-id="d568b-117">By default, this setting is taken from the journal name.</span></span> <span data-ttu-id="d568b-118">Ve výchozím nastavení je nastavení názvu deníku převzato z nastavení na stránce **Parametry hlavní knihy** při vytvoření názvu deníku.</span><span class="sxs-lookup"><span data-stu-id="d568b-118">By default, the setting for the journal name is taken from the setting on the **General ledger parameters** page when the journal name is created.</span></span> <span data-ttu-id="d568b-119">V následujících oddílech je vysvětleno, jak zapnout výpočet zpožděné daně pro právnické osoby, názvy deníků a záhlaví deníků.</span><span class="sxs-lookup"><span data-stu-id="d568b-119">The following sections explain how to turn on delayed tax calculation for legal entities, journal names, and journal headers.</span></span>

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a><span data-ttu-id="d568b-120">Zapnutí výpočtu opožděné daně na úrovni právnické osoby</span><span class="sxs-lookup"><span data-stu-id="d568b-120">Turn on delayed tax calculation at the legal entity level</span></span>

1. <span data-ttu-id="d568b-121">Přejděte na **Hlavní kniha \> Nastavení hlavní knihy \> Parametry hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="d568b-121">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="d568b-122">Na kartě **DPH** na pevné záložce **Obecné** nastavte možnost **Výpočet opožděné daně** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="d568b-122">On the **Sales tax** tab, on the **General** FastTab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Obrázek Parametry hlavní knihy](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a><span data-ttu-id="d568b-124">Zapnutí výpočtu opožděné daně na úrovni názvu deníku</span><span class="sxs-lookup"><span data-stu-id="d568b-124">Turn on delayed tax calculation at the journal name level</span></span>

1. <span data-ttu-id="d568b-125">Přejděte na položky **Hlavní kniha \> Nastavení deníku \> Názvy deníku**.</span><span class="sxs-lookup"><span data-stu-id="d568b-125">Go to **General ledger \> Journal setup \> Journal names**.</span></span>
2. <span data-ttu-id="d568b-126">Na pevné záložce **Obecné** v části **DPH** nastavte možnost **DVýpočet opožděné daně** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="d568b-126">On the **General** FastTab, in the **Sales tax** section, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Obrázek Názvy deníků](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a><span data-ttu-id="d568b-128">Zapnutí výpočtu opožděné daně na úrovni záhlaví deníku</span><span class="sxs-lookup"><span data-stu-id="d568b-128">Turn on delayed tax calculation at the journal header level</span></span>

1. <span data-ttu-id="d568b-129">Přejděte na **Hlavní kniha \> Položky deníku \> Hlavní deníky**.</span><span class="sxs-lookup"><span data-stu-id="d568b-129">Go to **General ledger \> Journal entries \> General journals**.</span></span>
2. <span data-ttu-id="d568b-130">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="d568b-130">Select **New**.</span></span>
3. <span data-ttu-id="d568b-131">Vyberte název deníku.</span><span class="sxs-lookup"><span data-stu-id="d568b-131">Select a journal name.</span></span>
4. <span data-ttu-id="d568b-132">Na kartě **Nastavení** nastavte možnost **Výpočet opožděné daně** na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="d568b-132">On the **Setup** tab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Obrázek stránky hlavního deníku](media/delayed-tax-calculation-journal-header.png)
