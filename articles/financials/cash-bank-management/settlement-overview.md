---
title: "Přehled vyrovnání"
description: "V tomto článku jsou obecné informace o procesu vyrovnání. Popisuje typy transakcí, které lze vyrovnat, kdy a jak lze transakce vyrovnat, a jaké jsou výsledky procesu vyrovnání."
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14551
ms.assetid: 0968fa71-5984-415b-8689-759a0136d5d1
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2f1f11a7f1340d408374e658ae616ffa99f3c911
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="settlement-overview"></a>Přehled vyrovnání

[!include [banner](../includes/banner.md)]

V tomto článku jsou obecné informace o procesu vyrovnání. Popisuje typy transakcí, které lze vyrovnat, kdy a jak lze transakce vyrovnat, a jaké jsou výsledky procesu vyrovnání.

Při vyrovnání transakce z jednoho dokumentu platí pro transakce na jiném dokumentu pro zvýšení nebo snížení zůstatku z jednotlivých dokumentů. Platbu lze například použít na fakturu. Různé typy transakcí lze vyrovnat v různých časech a prostřednictvím různých metod. Vyrovnání může také způsobit vygenerování nových transakcí.

## <a name="what-transactions-can-be-settled"></a>Transakce, které je možné vyrovnat
Vyrovnání v rámci závazků a pohledávek mohou být provedeny mezi všemi typy transakcí, které ovlivňují zůstatek dodavatele nebo zůstatek odběratele, jako jsou například faktury, platby, dobropisy a poplatky. Kterýkoliv typ transakce můžete vyrovnat s pohledem na jiný typ transakce. Například můžete vyrovnat platbu pro fakturu, dobropis pro fakturu, fakturu pro fakturu a platbu pro platbu. Můžete vyrovnat platby pro transakci ve stejné právnické osobě nebo v jiné právnické osobě. V organizacích, které využívají centralizovaný model platby vám může [vyrovnání mezi více společnostmi](set-up-centralized-payments.md) pomoci urychlit platební proces.

## <a name="when-to-settle-transactions"></a>Kdy vyrovnat transakce
Transakce je možné vyrovnat při zadání platby. Například při realizaci platby pro dodavatele obvykle vybíráte faktury, které chcete zaplatit. Výběrem faktur je označíte pro vyrovnání oproti platbě. Když pracovník pro platby pohledávek zaznamená platbu odběratele, může označit odpovídající faktury pro vyrovnání, které jsou založené na informacích dodaných s platbou odběratele. Stránka **Vyrovnat transakce** slouží k označení transakcí pro vyrovnání. Tuto stránku lze otevřít z každé nezaúčtované faktury či platby. Když je transakce zaúčtována, je zaúčtováno také vyrovnání. Transakce lze také vyrovnat po zaúčtování. Můžete zadat a zaúčtovat platbu odběratele, aniž byste ji vyrovnali pro jakoukoli fakturu. Můžete však nejprve provést průzkum, abyste se ujistili, že platba je vyrovnána proti správné faktuře. Stránku **Vyrovnat transakce** lze otevřít ze stránky **Všichni zákazníci** nebo **Všichni dodavatelé**, nebo ze stránky **Transakce** pro libovolného odběratele nebo dodavatele. Můžete také rezervovat zaúčtované zálohy pro fakturu označením platby k vyrovnání pro nákupní objednávku nebo prodejní objednávku. V tomto případě platby budete mít stále otevřený zůstatek, ale nemůže být vyrovnán proti další faktuře. Platba bude automaticky vyrovnána proti faktuře, která je vytvořena z nákupní objednávky nebo prodejní objednávky.

## <a name="how-to-settle-transactions"></a>Jak vyrovnat transakce
Transakce je možné vyrovnat ručně, automaticky nebo kombinací obou způsobů. Výběr metody vyrovnání závisí na obchodních procesech, které mohou být implementovány skrze nastavení vyrovnání v parametrech závazků a parametrech pohledávek. Vytvořením návrhu platby, který slouží k výběru faktur k úhradě, můžete vytvořit platby dodavatele a platby přímého debetu odběratelů. Návrh platby může být aktivován ručně, ale aplikace Microsoft Dynamics 365 for Finance and Operations automaticky označí vybrané faktury k vyrovnání při vytvoření plateb. Pokud jsou platby vytvořeny ručně, můžete použít stránku **Vyrovnat transakce** k výběru faktur k vyrovnání. Faktury je možné vybrat ručně nebo lze použít možnost **Označit podle priority**, kdy budou faktury automaticky označeny k vyrovnání. Možnost **Označit podle priority** je dostupná pouze pro pohledávky. Chcete-li tuto možnost použít, použijte stránku **Priorita vyrovnání** v parametrech pohledávky. Pokud úředník pro platby zadá platbu, ale nevyrovná ji, než platbu zaúčtuje, platba bude automaticky vyrovnána. Můžete zapnout automatické vyrovnání v parametrech pohledávek a parametrech závazků. Při použití automatického vyrovnání můžete použít předdefinované pořadí vyrovnání nebo můžete definovat vlastní pořadí priority vyrovnání v parametrech pohledávek. Tato funkce je k dispozici pouze pro pohledávky.

## <a name="results-of-settlement"></a>Výsledky vyrovnání
Jak dojde k vyrovnání transakce, je zůstatek pro jednotlivé transakce zvýšen nebo snížen podle potřeby. V typickém scénáři, kde jsou vyrovnány faktura a platba, se aktualizuje stav a zůstatek jednotlivých transakcí podle následujících pravidel:

-   Je-li částka platby větší, než částka faktury, snižuje se zůstatek faktury na 0,00 a faktura je uzavřena. Platba zůstane otevřená a zůstatek je částka, o který platba překročila částku faktury.
-   Je-li částka platby menší, než částka faktury, snižuje se zůstatek platby na 0,00 a platba je uzavřena. Faktura zůstane otevřená a zůstatek je částka, o který platba nedosáhla výše faktury.
-   Pokud je částka platby shodná s částkou faktury, platba a faktura je uzavřena a zůstatek obou bude 0,00.

Pokud [je platba menší než částka faktury](../accounts-payable/vendor-payments-partial-amount.md) z důvodu platební slevy, odpisu nebo nedoplatku, faktura a platba může být i nadále uzavřena v závislosti na nastavení vyrovnání v parametrech závazků a parametrech pohledávek. Vyrovnání může také vytvořit transakce. Vyrovnání faktury a platby může být například vytvořit platební slevu, realizovaný zisk nebo ztrátu, úpravy prodejní daně, odpisy a haléřové rozdíly.




