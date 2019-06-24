---
title: Chytrá doporučení
description: Toto téma vysvětluje, jak lze použít strojové učení pro poskytnutí doporučení pro práce a uchazeče o práci.
author: andreabichsel
manager: AnnBe
ms.date: 05/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 301e3213fa0988faba83ee42b840646a20c70a98
ms.sourcegitcommit: fcae2e7938d7dbd94b76b0948b084d90d5fc919c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/05/2019
ms.locfileid: "1620613"
---
# <a name="intelligent-recommendations"></a>Chytrá doporučení

[!include[banner](../includes/banner.md)]

Strojové učení může pomoci náborovým pracovníkům a náborovým manažerům k rychlé identifikaci nejlepších kandidátů na pozici. Také může pomoci potenciálním uchazečům najít pozici, která nejlépe odpovídá jejich profilu a zájmům. Když se tyto funkce používají a poskytuje se zpětná vazba, doporučení se zdokonalují.

> [!NOTE] 
> - Funkce chytrých doporučení jsou k dispozici pouze [s doplňkem Komplexní nábor](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/attract-comprehensive-hiring).
> - Funkce pojednávaná v tomto tématu je k dispozici jako součást verze Preview. Obsah a funkce se mohou změnit. Chcete-li použít tuto funkci, požádejte správce o její povolení pomocí **Centrum pro správu** v aplikaci Attract. Nastavte **Doporučení kandidáta**, **Doporučení práce** a **Doporučení potenciálního uchazeče** na **Zapnuto**. Další informace naleznete v tématu [Přístup k funkcím Preview v aplikaci Talent](./access-preview-feature.md). 


## <a name="candidate-recommendations"></a>Doporučení kandidáta

Vzhledem k tomu, že nabídky pracovních míst mohou přilákat stovky uchazečů, může být obtížné pro náborové pracovníky a manažery najít kandidáty, jejichž dovednosti a zkušenosti nejlépe odpovídají pozici. Analýzou vztahu mezi popisem práce a požadavky a údaji z životopisů a profilů kandidátů lze strojové učení využít k vypracování doporučení kandidátů. Doporučení kandidáta mohou pomoci náborovým pracovníkům a náborovým manažerům identifikovat špičkové talenty a posunout je do fáze pohovoru rychleji. Pro každou práci, pokud je více než deset kandidátů nebo uchazečů, kteří mají životopisy nebo kompletní profily, se kandidáti nebo uchazeči, kteří nejvíce splňují požadavky na práci, objeví v části **Uchazeči ke zvážení** na stránce **Práce**.

Pro jakéhokoliv doporučeného kandidáta můžete vybrat možnost **Zobrazit kandidáta** na kartě kandidáta, zkontrolovat profil kandidáta a provést akce s jeho/její žádostí. Můžete použít tlačítko se třemi tečkami (**...**) k otevření profilu kandidáta na nové kartě. Toto tlačítko také slouží k poskytnutí zpětné vazby o doporučení. Tímto způsobem pomůžete optimalizovat modul doporučení a vylepšit budoucí doporučení. Všechna doporučení, která se vám nelíbí, jsou odstraněna z části **Uchazeči ke zvážení**, když obnovíte stránku **Práce**. Kartu zpětné vazby můžete použít k označení, proč pro vás nebylo doporučení užitečné.

## <a name="job-recommendations"></a>Doporučení práce 

Pokud potenciální zaměstnanec použije kariérní web, aby se ucházel o zaměstnání, Attract doporučí další otevřené pozice v organizaci. Tato doporučení se zakládají na předchozích žádostech a životopisu a profilu potenciálního uchazeče. Tím pádem doporučení práce pomáhají uchazečům rychle identifikovat práce, které jsou pro ně nejvhodnější. Doporučení práce jsou poskytována uchazečům tehdy, pokud je na kariérním webu nabízeno více než deset pracovních pozic. Uchazeči mohou otevřít podrobnosti o nabídce zaměstnání z karty doporučení. Mohou také poskytnout zpětnou vazbu o doporučení za účelem vylepšení budoucích doporučení.

## <a name="prospect-recommendations"></a>Doporučení potenciálního uchazeče 

Když je k dispozici nová pozice, prohledávání všech vašich minulých uchazečů a celé sítě talentů může chvíli zabrat. Aby vám s tím aplikace Attract pomohla, můžete použít inteligentní algoritmy strojového učení. To znamená, že jakmile vytvoříte práci, Attract zreviduje všechny kandidáty a navrhne ty, kteří nejlépe vyhovují požadavkům. Chcete-li zobrazit tato doporučení, povolte pro práci fázi **Potenciální uchazeč**. To může trvat až minutu, než Attract projde celou databázi kandidátů a poskytne doporučení.

Doporučení budou zobrazeny jako karty na záložce **Potenciální uchazeči** všech prací, které mají povolenou fázi **Potenciální uchazeč**. Tyto karty uvádějí dovednosti, které se nacházejí v profilu potenciálního uchazeče, jakož i informace o kvalifikaci a vzdělání. Pokud najdete doporučení, které se vám líbí, můžete přidat kandidáta jako potenciálního uchazeče pro tuto práci.

> [!NOTE]
> Pokud jste v nedávné době začali používat Attract, budete muset počkat, až budete mít 10 nebo více uchazečů, kteří mají úplné profily nebo životopisy, než tuto funkci použijete.

Aby se předešlo případnému zkreslení doporučení, Attract pouze vyhledá profily kandidátů pro dovednosti, kvalifikace a další klíčová slova, která odpovídají popisu práce. Attract navíc před hodnocením odstraní osobní identifikaci informací z profilů kandidátů.
