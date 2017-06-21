---
title: "Nastavení mezipodnikového účetnictví"
description: "Toto téma vysvětluje, jak se nastavuje mezipodnikové účetnictví tak, abyste mohli používat mezipodnikové deníky k přidělování knih a finančních deníků, jako jsou každodenní deníky, deníky faktur dodavatele a platební deníky."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 506c7958a90bd5a891ea9859c679fcadb64a64d4
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="intercompany-accounting-setup"></a>Nastavení mezipodnikového účetnictví

[!include[banner](../includes/banner.md)]


Toto téma vysvětluje, jak se nastavuje mezipodnikové účetnictví tak, abyste mohli používat mezipodnikové deníky k přidělování knih a finančních deníků, jako jsou každodenní deníky, deníky faktur dodavatele a platební deníky.

Mezipodnikové deníky lze vytvářet podle řady scénářů, například pro každodenní deníky, deníky faktur dodavatele, přidělování hlavní knihy a centralizované platby. Chcete-li tyto scénáře povolit, je třeba nastavit mezipodnikové účetnictví.

## <a name="define-main-accounts"></a>Definování hlavních účtů
Nejprve je nutné vytvořit mezipodnikové hlavní účty, které se použijí pro účetní položky Závazky a Pohledávky. Je vhodné použít jedinečné hlavní účty pro každou společnost, aby se zjednodušilo odsouhlasení a eliminace mezipodnikových účetních položek. Pokud k identifikaci mezipodnikové strany používáte dimenzi obchodního partnera nebo protistrany, můžete tuto dimenzi definovat jako pevnou dimenzi v hlavním účtu, který je definován v mezipodnikovém účtování. Při nastavování hlavních účtů byste měli nastavit hodnotu v poli **Typ hlavního účtu** na **Rozvaha** na stránce **Hlavní účty**.

## <a name="define-journal-names"></a>Definování názvů deníků
Dále je třeba definovat název deníku. Nastavte hodnotu v poli **Typ deníku** na **Každodenní** na stránce **Názvy deníků**. Je vhodné používat konkrétní název deníku pro mezipodnikové účetnictví.

## <a name="define-intercompany-accounting-setup"></a>Definování nastavení mezipodnikového účetnictví
Stránka **Mezipodnikové účetnictví** slouží k vytvoření dvojic právnických osob, které mohou provádět vzájemné transakce. Nastavení Mezipodnikové účetnictví je sdílené, takže ho vidí všechny právnické osoby. Při vytváření nové dvojice právnických osob si musíte být vědomi, která právnická osoba je definována jako původní společnost versus cílové společnosti. Při zadávání mezipodnikových transakcí transakce určuje, která právnická osoba transakci zahajuje nebo od které transakce pochází. Mezipodnikové účtování je například nastavení pro USMF (původní) a USSI (cílová). Pokud je uživatel aktivní v USSI a zadá mezipodnikovou transakci s USMF, transakce se nezaúčtuje, protože mezipodnikové účetnictví je definováno pouze pro USMF, které je původcem. Pokud může být původcem transakce některá ze společností, budete muset vytvořit druhý pár právnických osob pro vzájemné nastavení. 

Vyberte **Účet má dáti (Pohledávky)** a **Dal účet (Závazky)** pro právnickou osobu, která je původcem i příjemcem. Definujte, který **Název deníku** bude použit při vytvoření transakce v cílové společnosti. Deník pro původní společnost je již znám, protože je vybrán uživatelem při vytváření mezipodnikových transakcí. 

Nakonec vyberte, které právnická osoba obdrží účetnictví na podporu částek, jako jsou platební slevy pro centralizované platby realizované zisky/ztráty. 

Vzájemný vztah lze snadno nastavit na stránce **Mezipodnikové účetnictví** pomocí tlačítka **Vytvořit vzájemný vztah** tlačítko po vytvoření prvního páru právnické osoby. Při vytvoření vzájemné dvojice budou informace o cílové společnosti zkopírovány do původní společnosti a naopak. Deníku definovaný pro cílovou společnost zůstane. Většina organizací používá stejné konvence pojmenování pro své názvy deníku takže název deníku je stejný. Pokud se název deníku liší, zobrazí se upozornění v poli s upozorněním, že deník neexistuje a lze vybrat jiný deník.




