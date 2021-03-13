---
title: Často kladené dotazy týkající se funkce Jeden doklad
description: Toto téma poskytuje odpovědi na časté otázky týkající se funkce Jeden doklad. Jedno číslo dokladu pro finanční deníky (deník hlavní knihy, deník dlouhodobého majetku, deník platby dodavatele a tak dále) slouží k zadání více transakcí hlavní knihy v rámci jednoho dokladu.
author: kweekley
manager: AnnBe
ms.date: 11/05/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerParameters, AssetProposalDepreciation
audience: Application User
ms.reviewer: roschlom
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-03-16
ms.dyn365.ops.version: 8.0.2
ms.openlocfilehash: 916f0172a2d7f9fad9dcd70b31f8ecf65e47b2c8
ms.sourcegitcommit: bd4763cc6088e114818e80bb1c27c6521b039743
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/02/2021
ms.locfileid: "5107742"
---
# <a name="one-voucher-faq"></a><span data-ttu-id="a50b8-104">Často kladené dotazy týkající se funkce Jeden doklad</span><span class="sxs-lookup"><span data-stu-id="a50b8-104">One voucher FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a50b8-105">Toto téma poskytuje odpovědi na časté otázky týkající se funkce Jeden doklad.</span><span class="sxs-lookup"><span data-stu-id="a50b8-105">This topic answers frequently asked questions about the One voucher functionality.</span></span> <span data-ttu-id="a50b8-106">Jeden doklad pro finanční deníky vám umožňuje zadat více transakcí dílčí knihy v kontextu jediného dokladu.</span><span class="sxs-lookup"><span data-stu-id="a50b8-106">One voucher for financial journals lets you enter multiple subledger transactions in the context of a single voucher.</span></span> <span data-ttu-id="a50b8-107">Deníky, které do tohoto dokladu můžete zahrnout, mohou být mimo jiné obecné deníky, deníky dlouhodobého majetku a deníky plateb od dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="a50b8-107">The journals that you can include in that voucher can be general journals, fixed asset journals, and vendor payment journals, among others.</span></span>

## <a name="when-will-the-one-voucher-functionality-be-deprecated"></a><span data-ttu-id="a50b8-108">Kdy bude ukončena funkce Jeden doklad?</span><span class="sxs-lookup"><span data-stu-id="a50b8-108">When will the One voucher functionality be deprecated?</span></span>

<span data-ttu-id="a50b8-109">Ačkoli společnost Microsoft nemůže poskytnout přesný odhad o tom, kdy bude funkce Jeden doklad zastaralá, bude pravděpodobně trvat nejméně dva roky, než dojde k ukončení podpory.</span><span class="sxs-lookup"><span data-stu-id="a50b8-109">Although Microsoft can't provide an accurate estimate about when the One voucher functionality will be deprecated, it will likely be at least two years before the deprecation occurs.</span></span>

<span data-ttu-id="a50b8-110">Jak je uvedeno v dokumentaci k Jednomu dokladu, řadu obchodních požadavků lze splnit pouze pomocí Jednoho dokladu.</span><span class="sxs-lookup"><span data-stu-id="a50b8-110">As is noted in the One voucher documentation, numerous business requirements can be met only by using One voucher.</span></span> <span data-ttu-id="a50b8-111">Microsoft musí zajistit, aby všechny identifikované obchodní požadavky mohly být v systému stále plněny i po ukončení podpory této funkce.</span><span class="sxs-lookup"><span data-stu-id="a50b8-111">Microsoft must ensure that all the identified business requirements can still be met in the system after the functionality is deprecated.</span></span> <span data-ttu-id="a50b8-112">Proto bude pravděpodobně nutné přidat nové funkce k vyplnění funkčních mezer.</span><span class="sxs-lookup"><span data-stu-id="a50b8-112">Therefore, new features will probably have to be added to fill functional gaps.</span></span>

<span data-ttu-id="a50b8-113">Po vyplnění všech funkčních mezer společnost Microsoft sdělí, že funkce bude zastaralá.</span><span class="sxs-lookup"><span data-stu-id="a50b8-113">After all functional gaps are filled, Microsoft will communicate that the feature will be deprecated.</span></span> <span data-ttu-id="a50b8-114">Zastarání však nebude účinné po dobu nejméně jednoho roku po tomto oznámení.</span><span class="sxs-lookup"><span data-stu-id="a50b8-114">However, the deprecation won't be effective for least one year after that communication.</span></span>

<span data-ttu-id="a50b8-115">Další informace naleznete v [dokumentaci k Jednomu dokladu](one-voucher.md).</span><span class="sxs-lookup"><span data-stu-id="a50b8-115">For more information, see the [One voucher documentation](one-voucher.md).</span></span>

## <a name="what-will-the-solution-that-replaces-one-voucher-look-like"></a><span data-ttu-id="a50b8-116">Jak bude vypadat řešení, které nahradí Jeden doklad?</span><span class="sxs-lookup"><span data-stu-id="a50b8-116">What will the solution that replaces One voucher look like?</span></span>

<span data-ttu-id="a50b8-117">Microsoft nemůže poskytnout konkrétní řešení, protože každá mezera mezi funkcemi je jiná a musí být hodnocena na základě obchodních požadavků.</span><span class="sxs-lookup"><span data-stu-id="a50b8-117">Microsoft can't provide a specific solution, because each feature gap is different and must be evaluated based on the business requirements.</span></span> <span data-ttu-id="a50b8-118">Některé funkční mezery budou pravděpodobně nahrazeny funkcemi, které pomohou splnit konkrétní obchodní požadavky.</span><span class="sxs-lookup"><span data-stu-id="a50b8-118">Some functional gaps will likely be replaced with features that help meet specific business requirements.</span></span> <span data-ttu-id="a50b8-119">Jiné mezery však mohou být vyplněny pokračováním v povolení zápisu do deníku, jako když je použit Jeden doklad, ale vylepšením systému lze podle potřeby sledovat více podrobností.</span><span class="sxs-lookup"><span data-stu-id="a50b8-119">However, other gaps might be filled by continuing to allow for entry in a journal, as when One voucher is used, but enhancing the system to track more detail as required.</span></span>

## <a name="where-can-i-track-the-progress-of-the-feature-gaps-being-filled"></a><span data-ttu-id="a50b8-120">Kde mohu sledovat průběh vyplňování mezer funkcí?</span><span class="sxs-lookup"><span data-stu-id="a50b8-120">Where can I track the progress of the feature gaps being filled?</span></span>

<span data-ttu-id="a50b8-121">Stejně jako u každé nové funkce musí zákazníci sledovat plán vydání a dokumentaci „Co je nového nebo změněného“.</span><span class="sxs-lookup"><span data-stu-id="a50b8-121">As for every new feature, customers must watch the Release plan and "What's new or changed" documentation.</span></span> <span data-ttu-id="a50b8-122">Každá funkce bude přidána do těchto dokumentů a poznámka bude označovat, že tato funkce je vyžadována ke splnění obchodního požadavku, který dříve vyžadoval funkci Jeden doklad.</span><span class="sxs-lookup"><span data-stu-id="a50b8-122">Each feature will be added to these documents, and a note will indicate that the feature is required to meet a business requirement that previously required the One voucher functionality.</span></span>

## <a name="when-the-deprecation-date-is-identified-where-will-it-be-communicated"></a><span data-ttu-id="a50b8-123">Až bude známé datum ukončení podpory, kde bude uvedeno?</span><span class="sxs-lookup"><span data-stu-id="a50b8-123">When the deprecation date is identified, where will it be communicated?</span></span>

<span data-ttu-id="a50b8-124">Ukončení podpory Jednoho dokladu je významnou změnou, která bude široce komunikována.</span><span class="sxs-lookup"><span data-stu-id="a50b8-124">The deprecation of One voucher is a significant change that will be widely communicated.</span></span> <span data-ttu-id="a50b8-125">Bude sděleno prostřednictvím dokumentace k produktu, příspěvku na blogu a oznámení na příslušných konferencích společnosti Microsoft, a to v dostatečném předstihu před datem, kdy ukončení podpory nabude účinnosti.</span><span class="sxs-lookup"><span data-stu-id="a50b8-125">It will be communicated through the product documentation, a blog post, and announcements at applicable Microsoft conferences, well in advance of the date when the deprecation takes effect.</span></span>
