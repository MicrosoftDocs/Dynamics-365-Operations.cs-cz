---
title: Zálohové faktury a zálohy
description: Toto téma nabízí popis a porovnání dvou metod, které organizace mohou použít pro platby záloh (zálohy).
author: abruer
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, PurchTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15871
ms.assetid: a0bb5220-73d4-48ae-84d0-46a171c224fa
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 64301ac540ce2e6e914b6b23668fddeb295ef84c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827979"
---
# <a name="prepayment-invoices-vs-prepayments"></a>Zálohové faktury a zálohy

[!include [banner](../includes/banner.md)]

Toto téma nabízí popis a porovnání dvou metod, které organizace mohou použít pro platby záloh (zálohy). První metoda vytvoří zálohovou fakturu, která je přidružená k nákupní objednávce. Druhá metoda vytvoří zálohové doklady deníku vytvořením položek deníku a jejich označením jako zálohový doklad deníku.

Organizace může vydávat zálohy (zálohové platby) dodavatelům za zboží nebo služby ještě před splněním objednávky zboží nebo služeb. K vydání záloh dodavatelům lze použít dvě metody. Kvůli minimalizaci rizika můžete sledovat zálohy definováním zálohy na nákupní objednávce. Pro tuto metodu je nutné vytvořit zálohovou fakturu, která je přidružená k nákupní objednávce. Tento způsob je označován jako zálohová fakturace. Organizace, které nechtějí sledovat zálohy tak detailně nebo které nepřijímají zálohové faktury od svého dodavatele, mohou namísto fakturace zálohy použít zálohový doklad deníku. Zálohový doklad deníku můžete vytvořit vytvořením položek deníku a jejich označením jako zálohový doklad deníku. Pro tuto metodu nelze sledovat, které zálohy jsou prováděné u dodavatele se kterými nákupními objednávkami. Můžete však označit zaúčtovanou zálohu k vyrovnání pro nákupní objednávku.

## <a name="when-to-use-prepayment-invoicing-vs-prepayments"></a>Kdy použít fakturace zálohy a zálohy

| Zálohové faktury                                                                | Zálohy                                                              |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Určete hodnotu zálohy na nákupní objednávce.                                    | Na nákupní objednávce není definována žádná hodnota zálohy.                    |
| Zálohová faktura a konečná faktura musejí být zaúčtovány.                       | Nesmí být zaúčtována žádná zálohová faktura.                                    |
| Odpovědnost za zálohu platí pro zálohový účet, ne pro účet závazků. | Odpovědnost za zálohu platí pro účet závazků.                  |
| Zůstatek dodavatele neodráží hodnotu zálohy během celého procesu.     | Zůstatek dodavatele odráží hodnotu zálohy během celého procesu. |
| Fakturace zálohy je k dispozici jen v části Závazky.                         | Zálohy jsou k dispozici v části Závazky a Pohledávky.    |

## <a name="overview-of-the-prepayment-process"></a>Přehled procesu záloh
Účetní praxe v mnoha zemích nebo oblastech vyžaduje, aby zálohy od odběratele nebo pro dodavatele nebyly zaúčtovány na běžných součtových účtech pro odběratele nebo dodavatele. Namísto toho se tyto platby záloh účtují do zvláštních účtů hlavní knihy určené pro platby záloh. Při vytvoření prodejní nebo nákupní objednávky je odběrateli nebo od dodavatele vystavena faktura. Při úhradě faktury dojde ke stornování zálohy a dokladu platby zálohy na DPH na účtech záloh hlavní knihy a částky faktury se automaticky zaúčtují na běžné součtové účty. Pokud chcete vytvořit zálohu, postupujte následovně.

1.  Nastavte účetní profily pro zálohy.
2.  V části Parametry pohledávek a Parametry závazků pod položkou **Hlavní kniha a DPH** vyberte nový účetní profil pomocí parametru **Účetní profil pro deník plateb se zálohou**.
3.  Vytvořte deník plateb a potom vytvořte novou platbu.
4.  Můžete platbu označit jako zálohu. Pokud je platba označena jako záloha, bude platba zaúčtována do účtů hlavní knihy, které jsou definovány v účetním profilu, který nastavíte podle kroku 1 a 2. Dále platí, že pokud je platba označena jako záloha, budou vypočteny daně. Některé úřady vyžadují zaplacení daní při zaznamenání zálohy, a to i v případě, že není k dispozici faktura.
5.  Zaúčtujte zálohu.
6.  Volitelné: Zálohu můžete před vytvořením faktury vyrovnat proti nákupní objednávce nebo prodejní objednávce. Na stránce prodejní nebo nákupní objednávky v podokně akcí použijte možnost **Vyrovnat transakce**.
7.  Jakmile dodavatel dodá zboží nebo služby, fakturu zaznamenejte. Pokud jste v kroku 6 vyrovnali zálohu oproti nákupní objednávce nebo prodejní objednávce, záloha se automaticky vyrovná oproti faktuře, kterou jste vytvořili. Pokud záloha nebyla vyrovnána oproti nákupní objednávce nebo prodejní objednávce, můžete ji ručně vyrovnat oproti faktuře s použitím možnosti **Vyrovnat transakce** na stránce odběratele nebo dodavatele. Částka zálohy je potom dočasně stornována z účtu hlavní knihy závazků/pohledávek. Dále pokud byly vypočteny daně, jsou stornovány, protože faktura obsahuje skutečné daně.

## <a name="overview-of-the-prepayment-invoicing-process"></a>Přehled procesu fakturace záloh
Zálohové faktury se při obchodování používají běžně. Dodavatel vystaví zálohové faktury a vyžaduje vklad při nákupu předtím, než je nákupní objednávka splněna. Někteří dodavatelé například mohou vyžadovat zálohu pro specifické zboží nebo služby. Pokud dodavatel vystaví fakturu vyžadující zálohu, můžete použít funkci fakturace záloh. Na nákupní objednávce lze definovat hodnotu zálohy, zálohová faktura je zaznamenána a uhrazena a poté je zálohová faktura použita na konečnou fakturu. Pokud chcete vytvořit zálohu, postupujte následovně.

1.  Nákupčí vytvoří, potvrdí a potom odešle nákupní objednávku, pro kterou dodavatel vyžaduje zálohu. Hodnota zálohy je definována na nákupní objednávce jako součást smlouvy.
2.  Dodavatel odešle zálohovou fakturu.
3.  Koordinátor závazků zaznamená zálohovou fakturu oproti nákupní objednávce a poté je zálohová faktura uhrazena.
4.  Dodavatel odešle žádost o platbu, která se označuje jako standardní faktura dodavatele. Jakmile dodavatel dodá zboží nebo služby a byly přijaty příslušné standardní faktury dodavatele, koordinátor závazků použije částku zálohy, která byla zaplacena podle standardní faktury.
5.  Koordinátor závazků zaplatí a vyrovná zbývající zůstatek standardní faktury.

## <a name="set-up-parameters-to-enable-the-prepayment-invoicing-process"></a>Nastavením parametrů povolte proces fakturace zálohy
Účet záloh musí být definován na kartě **Nákupní objednávka** stránky **Zaúčtování skladu** (**Řízení zásob \> Nastavení \> Zaúčtování \> Zaúčtování**). Po zaúčtování zálohové faktury bude aktualizován účet záloh, obvykle odepsáním částky. Zůstatek na účtu záloh bude stornován, když bude zaúčtována standardní faktura, která se použije na zálohovou fakturu. Pokud nevyrovnáte zálohovou fakturu s platbou před aplikací zálohové faktury na standardní fakturu, budou účetní položky ze zaúčtované zálohové faktury stornovány, když bude zaúčtována standardní faktura.

Souhrnný účet započtených závazků je definován v profilu **Zaúčtování dodavatele**. Chcete-li definovat výchozí profil zaúčtování, klikněte na **Závazky \> Nastavení \> Parametry závazků \> karta Hlavní kniha a DPH \> Profil zaúčtování se zálohovou fakturou dodavatele**.

**Zásady aplikace zálohy** vyjadřují, zda systém automaticky použije vypořádané zálohové faktury na konečnou fakturu, která byla vytvořena ručně. Faktury vytvořené pomocí datové entity nebudou odkazovat na **Zásady aplikace zálohy**. Na faktury, které byly vytvořeny pomocí datové entity, budete muset ručně použít vypořádané zálohové faktury. Chcete-li definovat zásady, přejděte na **Závazky \> Nastavení \> Parametry závazků \> karta Hlavní kniha a DPH \> Zásady aplikace zálohy**. Když je pole **Zásady aplikace zálohy** nastaveno na **Automatické**, bude zálohová faktura automaticky označena k vypořádání s konečnou fakturou. Pokud je pole nastaveno na hodnotu **Oznámení**, zobrazí se při vytvoření konečné faktury vizuální indikace, že je k dispozici zálohová faktura, kterou lze na konečnou fakturu použít.

## <a name="create-a-purchase-order-that-contains-prepayment-invoice-information"></a>Vytvoření nákupní objednávky, která obsahuje informace o zálohové faktuře
Když vám dodavatel řekne, že vyžaduje platbu předem za zboží a služby obsažené v nákupní objednávce, musíte definovat hodnotu zálohové platby pro příslušnou nákupní objednávku. Přejděte do nabídky **Závazky \> Běžné \> Nákupní objednávky \> Všechny nákupní objednávky** a najděte nákupní objednávku dodavatele. V podokně akcí vyberte kartu **Nákup** a poté vyberte možnost **Záloha**. Zadejte informace o záloze, včetně popisu, hodnoty zálohy, zda je záloha pevnou částkou nebo procentuální hodnotou, a ID kategorie zálohy. 

Upozorňujeme, že definice více záloh na nákupní objednávce není povolena. Pokud potřebujete na objednávce povolit více záloh, zaúčtujte platby pomocí deníku plateb namísto zálohové faktury.

Zálohu lze z nákupní objednávky odebrat, pokud jste již nezúčtovali platbu na zaúčtovanou zálohovou fakturu nebo nezaúčtovali standardní fakturu. Chcete-li z objednávky odebrat informace o záloze, přejděte do nabídky **Závazky \> Běžné \> Nákupní objednávky \> Všechny nákupní objednávky** a najděte nákupní objednávku dodavatele. V podokně akcí vyberte kartu **Nákup** a poté vyberte možnost **Odebrat zálohu**.

## <a name="create-and-post-a-prepayment-invoice"></a>Vytvořte a zaúčtujte zálohovou fakturu
Chcete-li zaznamenat zálohovou fakturu dodavatele, přejděte na stránku **Faktura dodavatele** výběrem možnosti **Zálohová faktura** na stránce **Nákupní objednávky** (**Závazky \> Běžné \> Nákupní objednávky \> Všechny nákupní objednávky \> karta Faktura\> Zálohová faktura**). Zadejte informace o zálohové faktuře, včetně čísla faktury. Množství nelze na zálohové faktuře změnit. Pokud dodavatel fakturoval částečnou částku hodnoty zálohy, která je definována v nákupní objednávce, můžete aktualizovat jednotkovou cenu tak, aby odrážela částečnou hodnotu.

Po zaúčtování zálohové faktury bude aktualizován zůstatek dodavatele a účet záloh. Hodnota **Aplikace zálohy** v definici zálohy obsažené v nákupní objednávce bude také aktualizována. Výchozí položky finanční dimenze pro zaúčtovaný doklad o záloze budou převzaty z informací v záhlaví nákupní objednávky.

## <a name="post-and-settle-payments-for-the-prepayment-invoice"></a>Zaúčtování a vyrovnání plateb za zálohovou fakturu
Následně bude zálohová faktura zaplacena na stránce **Deník plateb**. Chcete-li zobrazit deníky plateb, klikněte na **Závazky \> Deníky \> Platby \> Deník plateb**. Po zaúčtování vypořádání platby na zálohovou fakturu bude aktualizována hodnota **Aplikace zbývající zálohy** nákupní objednávky.

Před zaúčtováním standardní faktury k zálohové faktuře můžete zrušit vyrovnání platby ze zálohové faktury. Avšak poté, co je standardní faktura použita na zálohovou fakturu, již není vyrovnání platby ze zálohové faktury možné zrušit.

## <a name="post-the-standard-vendor-invoice-for-the-purchase-order-and-apply-the-prepayment-invoice-to-the-standard-invoice"></a>Zaúčtujte standardní fakturu dodavatele pro nákupní objednávku a použijte zálohovou fakturu na standardní fakturu
Zapište standardní fakturu obdrženou od dodavatele. V rámci tohoto procesu můžete na fakturu dodavatele použít vyrovnanou zálohovou fakturu tak, aby byla hodnota faktury snížena o částku, která již byla zaplacena. Uplatnění zálohové faktury na fakturu dodavatele zajistí, že budou stornovány účetní záznamy ze zálohové faktury.

## <a name="application-of-the-prepayment-invoice-after-posting-the-standard-invoice"></a>Aplikace zálohové faktury po zaúčtování standardní faktury
Pokud zapomenete uplatnit zálohu na standardní fakturu dodavatele v době zaúčtování faktury dodavatele, bude vyrovnaná platba k dispozici pro uplatnění na další faktury od tohoto dodavatele, a to na stránce **Dodavatelé** (**Závazky \> Běžné \> Dodavatelé \> Všichni dodavatelé \> karta Faktura \> Použít**).

## <a name="reversal-of-the-prepayment-application-process"></a>Stornování procesu aplikace zálohy
Pokud potřebujete zrušit vyrovnání nebo stornovat použití zálohové faktury na standardní fakturu, vyberte akci **Stornovat** na stránce **Dodavatelé** (**Závazky \> Běžné \> Dodavatelé \> Všichni dodavatelé\> karta Faktura \> Stornovat**). Po zrušení aplikace zálohy můžete zálohu použít na jinou standardní fakturu. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]