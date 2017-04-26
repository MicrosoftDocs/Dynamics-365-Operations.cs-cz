---
title: "Zálohové faktury a zálohy"
description: "Tento článek nabízí popis a porovnání dvou metod, které organizace mohou použít pro platby záloh (zálohy). Pro jednu metodu je nutné vytvořit zálohovou fakturu, která je přidružená k nákupní objednávce. Pro druhou můžete zálohový doklad deníku vytvořit vytvořením položek deníku a jejich označením jako zálohový doklad deníku."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, PurchTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15871
ms.assetid: a0bb5220-73d4-48ae-84d0-46a171c224fa
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 44d51807cd6bb64ae2c4bef58d8a445417ffa3a9
ms.openlocfilehash: 770a6fba8a27e9403235929b7e8cd547cc522486
ms.lasthandoff: 03/31/2017


---

# <a name="prepayment-invoices-vs-prepayments"></a>Zálohové faktury a zálohy

[!include[banner](../includes/banner.md)]


Tento článek nabízí popis a porovnání dvou metod, které organizace mohou použít pro platby záloh (zálohy). Pro jednu metodu je nutné vytvořit zálohovou fakturu, která je přidružená k nákupní objednávce. Pro druhou můžete zálohový doklad deníku vytvořit vytvořením položek deníku a jejich označením jako zálohový doklad deníku.

Organizace může vydávat zálohy (zálohové platby) dodavatelům za zboží nebo služby ještě před splněním objednávky zboží nebo služeb. K vydání záloh dodavatelům lze použít dvě metody. Kvůli minimalizaci rizika můžete sledovat zálohy definováním zálohy na nákupní objednávce. Pro tuto metodu je nutné vytvořit zálohovou fakturu, která je přidružená k nákupní objednávce. Tento způsob je označován jako zálohová fakturace. Organizace, které nechtějí sledovat zálohy tak detailně nebo které nepřijímají zálohové faktury od svého dodavatele, mohou namísto fakturace zálohy použít zálohový doklad deníku. Zálohový doklad deníku můžete vytvořit vytvořením položek deníku a jejich označením jako zálohový doklad deníku. Pro tuto metodu nelze sledovat, které zálohy jsou prováděné u dodavatele se kterými nákupními objednávkami. Můžete však označit zaúčtovanou zálohu k vyrovnání pro nákupní objednávku.

## <a name="when-to-use-prepayment-invoicing-vs-prepayments"></a>Kdy použít fakturace zálohy a zálohy
| Zálohové faktury                                                                | Zálohy                                                              |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Určete hodnotu zálohy na nákupní objednávce.                                    | Na nákupní objednávce není definována žádná hodnota zálohy.                    |
| Klíč: Musí být zaúčtována zálohová faktura a konečná faktura.                       | Nesmí být zaúčtována žádná zálohová faktura.                                    |
| Odpovědnost za zálohu platí pro zálohový účet, ne pro účet závazků. | Odpovědnost za zálohu platí pro účet závazků.                  |
| Zůstatek dodavatele neodráží hodnotu zálohy během celého procesu.     | Zůstatek dodavatele odráží hodnotu zálohy během celého procesu. |
| Fakturace zálohy je k dispozici jen v části Závazky.                         | Zálohy jsou k dispozici v části Závazky a Pohledávky.    |

## <a name="overview-of-the-prepayment-process"></a>Přehled procesu záloh
Účetní praxe v mnoha zemích nebo oblastech vyžaduje, aby zálohy od odběratele nebo pro dodavatele nebyly zaúčtovány na běžných součtových účtech pro odběratele nebo dodavatele. Namísto toho se tyto platby záloh účtují do zvláštních účtů hlavní knihy určené pro platby záloh. Při vytvoření prodejní nebo nákupní objednávky je odběrateli nebo od dodavatele vystavena faktura. Při úhradě faktury dojde ke stornování zálohy a dokladu platby zálohy na DPH na účtech záloh hlavní knihy a částky faktury se automaticky zaúčtují na běžné součtové účty. Pokud chcete vytvořit zálohu, postupujte následovně.

1.  Nastavte účetní profily pro zálohy.
2.  V části Parametry pohledávek a Parametry závazků pod položkou **Hlavní kniha a DPH** vyberte nový účetní profil pomocí parametru **Účetní profil pro deník plateb se zálohou**.
3.  Vytvořte deník plateb a potom vytvořte novou platbu.
4.  Můžete platbu označit jako zálohu. Platba je označena jako záloha, platba se zaúčtuje na účty hlavní knihy, které jsou definovány na účetní profil, který jste vytvořili v krocích 1 a 2. Navíc pokud je platba je označena jako záloha, budou daně vypočítány. Některé úřady vyžadují zaplacení daní při zaznamenání zálohy, a to i v případě, že není k dispozici faktura.
5.  Zaúčtujte zálohu.
6.  Volitelné: Můžete vyrovnat zálohy proti nákupní objednávka nebo prodejní objednávce před vytvořením faktury. Prodejní objednávky nebo nákupní objednávky stránky, v podokně akcí pomocí **vyrovnat transakce**.
7.  Jakmile dodavatel dodá zboží nebo služby, fakturu zaznamenejte. Pokud jste v kroku 6 vyrovnali zálohu oproti nákupní objednávce nebo prodejní objednávce, záloha se automaticky vyrovná oproti faktuře, kterou jste vytvořili. Pokud záloha nebyla vyrovnána oproti nákupní objednávce nebo prodejní objednávce, můžete ji ručně vyrovnat oproti faktuře s použitím možnosti **Vyrovnat transakce** na stránce odběratele nebo dodavatele. Částka zálohy je potom dočasně stornována z účtu hlavní knihy závazků/pohledávek. Dále pokud byly vypočteny daně, jsou stornovány, protože faktura obsahuje skutečné daně.

## <a name="overview-of-the-prepayment-invoicing-process"></a>Přehled procesu fakturace záloh
Zálohové faktury se při obchodování používají běžně. Dodavatel vystaví zálohové faktury a vyžaduje vklad při nákupu předtím, než je nákupní objednávka splněna. Někteří dodavatelé například mohou vyžadovat zálohu pro specifické zboží nebo služby. Pokud dodavatel vystaví fakturu vyžadující zálohu, můžete použít funkci fakturace záloh. Na nákupní objednávce lze definovat hodnotu zálohy, zálohová faktura je zaznamenána a uhrazena a poté je zálohová faktura použita na konečnou fakturu. Pokud chcete vytvořit zálohu, postupujte následovně.

1.  Nákupčí vytvoří, potvrdí a potom odešle nákupní objednávku, pro kterou dodavatel vyžaduje zálohu. Hodnota zálohy je definována na nákupní objednávce jako součást smlouvy.
2.  Dodavatel odešle zálohovou fakturu.
3.  Koordinátor závazků zaznamená zálohovou fakturu oproti nákupní objednávce a poté je zálohová faktura uhrazena.
4.  Jakmile dodavatel dodá zboží nebo služby a budou přijaty příslušné faktury dodavatele, koordinátor závazků použije částku zálohy, která byla zaplacena podle faktury.
5.  Koordinátor závazků zaplatí a vyrovná zbývající zůstatek faktury.





