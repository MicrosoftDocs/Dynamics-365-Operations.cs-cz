---
title: "Nastavení mezipodnikového účetnictví"
description: "Toto téma vysvětluje, jak nastavit mezipodnikové účetnictví, takže můžete provádět mezipodnikové deníky přidělení hlavní knihy a finanční deníky, například deníky, deníky faktur dodavatele a deníky plateb."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerInterCompany
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15761
ms.assetid: 1362297b-7a51-4930-b822-2b204a2e3c37
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 5fd279327013f26230146be38e23e9955c6f12c7
ms.lasthandoff: 03/31/2017


---

# <a name="intercompany-accounting-setup"></a>Nastavení mezipodnikového účetnictví

[!include[banner](../includes/banner.md)]


Toto téma vysvětluje, jak nastavit mezipodnikové účetnictví, takže můžete provádět mezipodnikové deníky přidělení hlavní knihy a finanční deníky, například deníky, deníky faktur dodavatele a deníky plateb.

Mezipodnikových deníků lze vytvořit v různých situacích, jako například pro denní deníky, deníky faktur dodavatele, přidělení hlavní knihy a centralizované platby. Chcete-li tyto scénáře povolit, je třeba nastavit mezipodnikové účetnictví.

## <a name="define-main-accounts"></a>Definování hlavních účtů
Nejprve je nutné vytvořit mezipodnikové hlavní účty, které se použijí pro účetní položky Závazky a Pohledávky. Je vhodné použít jedinečné hlavní účty pro každou společnost, aby se zjednodušilo odsouhlasení a eliminace mezipodnikových účetních položek. Pokud používáte k identifikaci mezipodnikové strana obchodního partnera nebo protějšek dimenze, můžete definovat tuto dimenzi jako pevná dimenze na hlavní účet, který je definován v mezipodnikové účetnictví. Při nastavení hlavních účtů byste měli nastavit **typ účtu hlavní** na **rozvaha** na **hlavní účty** stránky.

## <a name="define-journal-names"></a>Definování názvů deníků
Dále je třeba definovat název deníku. Nastavit **typ deníku** na **denní** na **názvy deníku** stránky. Je vhodné používat konkrétní název deníku pro mezipodnikové účetnictví.

## <a name="define-intercompany-accounting-setup"></a>Definovat nastavení mezipodnikového účetnictví
**Mezipodnikové účetnictví** stránky se používá k vytvoření dvojice právnických osob, které mohou provádět transakce s sebou. Mezipodnikové účtování nastavení sdílen, instalační program je viditelné ve všech právnických osobách. Při vytváření nové dvojice právnické osoby, zajistěte, že jste si vědomi které právnická osoba je definována jako původní společnost versus cílové společnosti. Při zadávání mezipodnikové transakce, transakce Určuje, které právnické osoby je zahájení nebo původní transakce. Mezipodnikové účtování je například nastavit USMF (původem) a USSI (cíl). Pokud uživatel zadá mezipodnikovou transakci s USMF a je aktivní v USSI transakce nezaúčtuje protože mezipodnikové účetnictví je definována pouze pro USMF je původcem. Transakce může pocházet buď společnosti, musíte vytvořit druhý pár právnické osoby pro vzájemné nastavení. 

Vyberte **účet má dáti (Pohledávky)** a **Dal účet (kvůli)** pro právnickou osobu výchozím a cílovým. Definujte, které **název deníku** bude použit při vytvoření transakce v cílové společnosti. Deník pro původní společnost je již znám, protože je vybrán uživatelem při vytváření mezipodnikových transakcí. 

Nakonec vyberte, které právnická osoba obdrží účetní pro podporu částky, například platební slevy pro centralizované platby realizované zisky/ztráty. 

Vzájemných vztahů lze snadno nastavit na **mezipodnikové účetnictví** stránku pomocí **vytvoření vzájemného vztahu** tlačítko po vytvoření první pár právnické osoby. Při vzájemném pár informací o cílové společnosti zkopírován na původní společnost a naopak. Deníku definovány pro cílovou společnost zůstane. Většina organizací používá stejné konvence pro názvy deníku tak, aby název deníku je stejný. Název deníku se liší, zobrazí se upozornění na pole s upozorněním, který neexistuje v deníku a jiný Deník lze vybrat.




