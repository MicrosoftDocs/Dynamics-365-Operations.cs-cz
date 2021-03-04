---
title: Přehled vyrovnání
description: V tomto tématu jsou obecné informace o procesu vyrovnání. Popisuje, které typy transakcí mohou být vypořádány, a načasování a proces jejich vypořádání. Popisuje také výsledky procesu vypořádání.
author: kweekley
manager: AnnBe
ms.date: 04/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14551
ms.assetid: 0968fa71-5984-415b-8689-759a0136d5d1
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 650b0ef0123cf9acf42c2e7460693b555897744f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441144"
---
# <a name="settlement-overview"></a>Přehled vyrovnání

[!include [banner](../includes/banner.md)]

V tomto tématu jsou obecné informace o procesu vyrovnání. Popisuje, které typy transakcí mohou být vypořádány, a načasování a proces jejich vypořádání. Popisuje také výsledky procesu vypořádání.

Při vyrovnání transakce z jednoho dokumentu platí pro transakce na jiném dokumentu pro zvýšení nebo snížení zůstatku z jednotlivých dokumentů. Platbu lze například použít na fakturu. Různé typy transakcí lze vyrovnat v různých časech a prostřednictvím různých metod. Proces vyrovnání může také způsobit vygenerování nových transakcí.

## <a name="what-transactions-can-be-settled"></a>Transakce, které je možné vyrovnat

Vyrovnání v rámci závazků a pohledávek mohou být provedena mezi všemi typy transakcí, které ovlivňují zůstatek dodavatele nebo zůstatek odběratele, jako jsou například faktury, platby, dobropisy a poplatky. Tyto typy transakcí mohou zahrnovat faktury, platby, dobropisy a poplatky. Kterýkoliv typ transakce můžete vyrovnat s pohledem na jiný typ transakce. Například můžete vyrovnat platbu pro fakturu, dobropis pro fakturu, fakturu pro fakturu a platbu pro platbu.

Můžete vyrovnat platby pro transakci ve stejné právnické osobě nebo v jiné právnické osobě. V organizacích, které využívají centralizovaný model platby vám může [vyrovnání mezi více společnostmi](set-up-centralized-payments.md) pomoci urychlit platební proces.

## <a name="when-to-settle-transactions"></a>Kdy vyrovnat transakce

Transakce lze vyrovnat při zadávání plateb. Například při realizaci platby pro dodavatele obvykle vybíráte faktury, které chcete zaplatit. Výběrem faktur je označíte pro vyrovnání oproti platbě. Když pracovník pro pohledávky zaznamená platby odběratele, může označit odpovídající faktury pro vyrovnání, které jsou založené na informacích dodaných s každou platbou odběratele. Stránka **Vyrovnat transakce** slouží k označení transakcí pro vyrovnání. Tuto stránku můžete otevřít z každé nezaúčtované faktury či platby. Když je transakce zaúčtována, je zaúčtováno také vyrovnání. 

Transakce lze také vyrovnat po zaúčtování. Můžete zadat a zaúčtovat platbu odběratele, aniž byste ji vyrovnali pro jakoukoli fakturu. Můžete se však chtít ujistit, že je platba vypořádána proti správné faktuře ještě před tím, než vypořádání zaúčtujete. Stránku **Vyrovnat transakce** lze otevřít ze stránky **Všichni zákazníci** nebo **Všichni dodavatelé**, nebo ze stránky **Transakce** pro libovolného odběratele nebo dodavatele.

Můžete také rezervovat zaúčtované zálohy pro fakturu označením platby k vyrovnání pro nákupní objednávku nebo prodejní objednávku. V tomto případě platby budete mít stále otevřený zůstatek, ale nemůže být vyrovnán proti další faktuře. Platba bude automaticky vyrovnána proti faktuře, která je vytvořena z nákupní objednávky nebo prodejní objednávky.

## <a name="how-to-settle-transactions"></a>Jak vyrovnat transakce

Transakce je možné vyrovnat ručně, automaticky nebo kombinací obou způsobů. Výběr metody vypořádání závisí na vašich obchodních procesech. Na stránce **Parametry pohledávek** a **Parametry závazků** stránky můžete proces vypořádání nakonfigurovat tak, aby byl v souladu s těmito obchodními procesy.

Vytvořením návrhu platby, který slouží k výběru faktur k úhradě, můžete vytvořit platby dodavatele. Návrh platby se používá k výběru faktur k úhradě. Návrh platby lze spustit ručně a systém následně automaticky označí vybrané faktury k vyrovnání při vytvoření plateb.

Pokud jsou platby vytvořeny ručně, můžete použít stránku **Vyrovnat transakce** k výběru faktur k vyrovnání. Faktury je možné vybrat ručně nebo lze použít možnost **Označit podle priority**, kdy budou faktury automaticky označeny k vyrovnání. Možnost **Označit podle priority** je dostupná pouze pro pohledávky. Tuto možnost můžete zapnout na kartě **Priorita vypořádání** na stránce **Parametry pohledávek**.

Pokud úředník pro platby zadá platbu, ale nevyrovná ji, než platbu zaúčtuje, platba bude automaticky vyrovnána. Můžete zapnout automatické vyrovnání na stránkcáh **Parametry pohledávek** a **Parametry závazků**. Automatické vypořádání vypořádává transakce pouze u stejné právnické osoby. Nevyrovnává transakce napříč několika právnickými osobami.

Při použití automatického vyrovnání můžete použít předdefinovanou prioritu vypořádání nebo můžete definovat vlastní prioritu na stránce **Parametry pohledávek**. Tato funkce je k dispozici pouze pro pohledávky.

## <a name="results-of-settlement"></a>Výsledky vyrovnání

Jak dojde k vyrovnání transakce, je zůstatek pro jednotlivé transakce zvýšen nebo snížen podle potřeby. Obvykle tam, kde jsou vyrovnány faktura a platba, se aktualizuje stav a zůstatek jednotlivých transakcí podle následujících pravidel:

- Je-li částka platby větší, než částka faktury, snižuje se zůstatek faktury na 0,00 a faktura je uzavřena. Platba zůstane otevřená a zůstatek je rozdíl mezi částkou platby a částkou faktury.
- Je-li částka platby menší, než částka faktury, snižuje se zůstatek platby na 0,00 a platba je uzavřena. Faktura zůstane otevřená a zůstatek je rozdíl mezi částkou faktury a částkou platby.
- Pokud je částka platby shodná s částkou faktury, platba a faktura je uzavřena a zůstatek obou se zredukuje na 0,00.

Pokud je [výše platby menší než částka faktury](../accounts-payable/vendor-payments-partial-amount.md) z důvodu platební slevy, odpisu nebo nedoplatku, faktura a platba může být i nadále uzavřena v závislosti na tom, jak je nakonfigurováno vyrovnání na stránkách **Parametry pohledávek** a **Parametry závazků**.

Vyrovnání může také vytvořit transakce. Vyrovnání faktury a platby může být například vytvořit platební slevu, realizovaný zisk nebo ztrátu, úpravy prodejní daně, odpisy a haléřové rozdíly.

## <a name="identifying-marked-transactions-during-settlement"></a>Identifikace označených transakcí během vypořádání

Při pokusu o vypořádání transakce si můžete všimnout symbolu, který označuje, že transakce je označena na jiném místě. V tomto případě můžete vybrat transakci na stránce **Vypořádat transakce** a poté vybrat možnosti **Dotaz \> Vypořádání z okna vypořádání**. Zobrazení tohoto dotazu zobrazí deníky, prodejní objednávky, faktury, návrhy plateb a místa zákazníků, která by mohla blokovat vypořádání transakce. Chcete-li tento problém vyřešit, můžete vybrat odkaz, který přejde přímo z dotazu na blokované místo. Poté můžete dokument aktualizovat úpravami, které jsou potřebné k jeho vyřešení. Můžete také použít indikátor **Označeno** k identifikaci dalších dokumentů, které jsou obsaženy ve stejném místě blokování.

## <a name="additional-resources"></a>Další prostředky

- [Vyrovnání zůstatku](settle-remainder.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]