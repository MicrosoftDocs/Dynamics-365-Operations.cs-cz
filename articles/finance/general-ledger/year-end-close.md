---
title: Roční uzávěrka
description: Toto téma popisuje požadované nastavení a postup pro spuštění procesu roční uzávěrky hlavní knihy.
author: kweekley
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: roschlom
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cdb81df1701851330b0501c03e41eb10e639bc77
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842313"
---
# <a name="year-end-close"></a>Roční uzávěrka

[!include [banner](../includes/banner.md)]

Toto téma popisuje požadované nastavení a postup pro spuštění procesu roční uzávěrky hlavní knihy. 

Na konci fiskálního roku je nutné spustit proces roční uzávěrky k převodu počátečních zůstatků do nového roku. Většina organizací spouští proces roční uzávěrky několikrát. Při prvním spuštění jde o získání zůstatků přesunutých do nového fiskálního roku. Roční uzávěrku lze potom spustit znovu, a to tolikrát, kolikrát je třeba, a přesunout zůstatky z položek úprav do nového fiskálního roku. 

Během procesu roční uzávěrky mohou být vytvořeny dva typy možných transakcí. Počáteční transakce je vždy vygenerována a slouží k vytváření počátečních zůstatků v novém fiskálním roce. Počáteční transakce zobrazí zůstatky účtů rozvahového účtu v novém fiskálním roce a zůstatky ze zůstatků účtu hlavní knihy zisků a ztrát na účtu hlavní knihy pozdržených příjmů v novém fiskálním roce. Uzávěrková transakce je vytvořena volitelně, aby bylo možné uvést zůstatky účtů zisků a ztrát na nulu ve fiskálním roce, který je uzavírán.

## <a name="prepare-to-run-the-year-end-close"></a>Příprava ke spuštění roční uzávěrky
Před spuštěním procesu roční uzávěrky ověřte následující nastavení: 

Na stránce **Hlavní účet** proveďte toto:

-   Ověřte, že je **Typ hlavního účtu** správně definován pro každý hlavní účet. Typ hlavního účtu se používá k určení, zda zůstatek hlavního účtu bude posunut dopředu jako počáteční zůstatek nebo uzavřen v pozdržených příjmech v počáteční transakci.
-   Pole **Počáteční účet** lze použít k převodu zůstatku hlavního účtu do nového hlavního účtu během roční uzávěrky. Nový hlavní účet je zadán do pole **Počáteční účet**. Obvykle se to používá pro rozvahové hlavní účty, když je hlavní účet deaktivován a nový hlavní účet se používá pro nový fiskální rok.

Na stránce **Parametry hlavní knihy** pod položkou **Uzávěrka fiskálního roku**:

-   Možnost **Odstranit transakce roční závěrky** se používá k určení, zda počáteční transakce generovaná systémem z předchozí roční uzávěrky má být odstraněna, když je roční uzávěrka spuštěna znovu. Pokud je tato možnost nastavena na hodnotu **Ano**, předchozí počáteční transakce je odstraněna a nová počáteční transakce se vytvoří na základě aktuálních zůstatků. Pokud je tato možnost nastavena na hodnotu **Ne**, předchozí počáteční transakce je zachována a vytvoří se další počáteční transakce k přesunutí zůstatků dopředu z transakcí úprav zaúčtovaných po předchozí roční uzávěrce.
-   Možnost **Vytvořit uzávěrkové transakce při převodu** se používá k vytvoření uzávěrkových transakcí ve fiskálním roku, který je uzavírán, aby zůstatky účtů zisků a ztrát mohly vykazovat nulu. Pokud je tato možnost nastavena na **Ano**, je vytvořena jak počáteční transakce, tak uzávěrková transakce. Pokud je tato možnost nastavena na **Ne**, je vytvořena pouze počáteční transakce v dalším fiskálním roku k převodu zůstatků. Zůstatky účtu zisků a ztrát zůstávají na konci fiskálního roku.
-   Možnost **Nastavit stav fiskálního roku na trvale uzavřený** slouží k nastavení stavu fiskálního roku „trvale uzavřený“. Toto nastavení používejte opatrně, protože žádné období se stavem „trvale uzavřeno“ nelze znovu otevřít, takže nelze zaúčtovat úpravy do fiskálního roku. Je doporučeno nastavit hodnotu **Ne**.
-   Možnost **Číslo dokladu musí být vyplněno** se používá k definování, zda je číslo dokladu požadováno při spuštění procesu roční uzávěrky. Doporučujeme vyžadovat číslo dokladu, aby bylo možné snadno identifikovat počáteční transakci.

Na stránce **Fiskální kalendář**:

-   Příští fiskální rok musí existovat před spuštěním roční uzávěrky. Příští fiskální rok je vyžadován při vytvoření počátečních zůstatků v počátečním období.

Na stránce **Kalendář hlavní knihy**:

-   Volitelné: Jednotlivá fiskální období pro fiskální rok, který je uzavírán, lze nastavit na hodnotu **Blokováno**, chcete-li zabránit v zadávání nových transakcí. Při zjištění položek úprav lze znovu otevřít blokovaná období a zaúčtovat položky úprav, a to i v případě, že již byl spuštěn proces roční uzávěrky.

## <a name="define-year-end-close-templates"></a>Definování šablon roční uzávěrky
Po konfiguraci systému můžete spustit proces roční uzávěrky. Na stránce **Roční uzávěrka** lze definovat šablonu pro skupinu právnických osob, pro kterou bude roční uzávěrka spuštěna. Tato šablona se znovu použije u každé roční uzávěrky, při změně v organizaci již však lze upravit. 

Nejprve definujte **Název skupiny** pro šablonu a vyberte fiskální kalendář. Název skupiny by měl označovat skupinu zahrnutých právnických osob.  Například šablona může nastavena na základě zeměpisné polohy a může zahrnovat samostatné skupiny vytvořené pro právnické osoby Severní Ameriky, právnické osoby zemí EMEA a právnické osoby APAC. 

Potom lze tyto právnické osoby přidat do šablony. Právnické osoby lze přidat zvolením organizační hierarchie nebo právnických osob. Pokud je vybrána organizační hierarchie, do šablony budou přidány pouze právnické osoby v rámci hierarchie, která používá vybraný fiskální kalendář. Při přidávání právnických osob do šablony mohou být přidány pouze právnické osoby se stejným fiskálním kalendářem. Stejný fiskální kalendář je vyžadován, protože se roční uzávěrka spouští zvolením fiskálního roku, který se může kalendář od kalendáře lišit. 

Po přidání právnických osob se definujte hlavní účty pozdržených příjmů pro každou právnickou osobu. Pole **Datum poslední roční uzávěrky** bude aktualizováno při každém spuštění roční uzávěrky pro danou právnickou osobu. 

Karta **Finanční dimenze** slouží k definování, které finanční dimenze budou použity v počáteční transakci. Nastavení, která definujete, se týkají pouze právnické osoby vybrané v mřížce **Právnické osoby**. Toto nastavení zopakujete pro každou právnickou osobu v mřížce. 

Možnost **Převést dimenze rozvahy** slouží k definování, zda finanční dimenze v transakcích zaúčtovaných na rozvahové účty mají být spravovány v počáteční transakci. Je doporučeno tuto možnost nastavit na hodnotu **Ano**. Možnost **Převést dimenze zisků a ztrát** slouží k definování, které finanční dimenze v transakcích zaúčtovaných na účtu zisků a ztrát budou převedeny do hlavního účtu pozdržených příjmů. Nejprve určete finanční dimenze, které jsou relevantní pro vybranou právnickou osobu. Zahrnovalo by to zahrnovalo všechny finanční dimenze zaúčtované v daném roce i v případě, že finanční dimenze není součástí aktivní účetní struktury. Dále určete každou dimenzi jako **Zavřít jedno** nebo **Uzavřít vše**.  Výchozí hodnota je **Uzavřít vše**, která udržuje původní hodnoty finanční dimenze ze zaúčtovaných transakcí a používá je pro vytvoření počátečních zůstatků pro účet pozdržených příjmů. Vytvoří se samostatné počáteční zůstatky pozdržených příjmů pro každou jedinečnou kombinaci hodnot finančních dimenzí. Pokud je zvolena možnost **Zavřít jedno**, všechny transakce zaúčtované s touto finanční dimenzí budou shrnuty do počátečního zůstatku pozdržených příjmů pro hodnotu dimenze zadanou v poli po **Zavřít jedno**. Předpokládejme například, že s účetní strukturou Hlavní účet – oddělení byly zaúčtovány všechny transakce pro daný fiskální rok. Ve finanční dimenzi oddělení v šabloně je vybrána možnost **Zavřít jedno** a je zadána hodnota 100. Pokud celkový příjem u všech transakcí zaúčtovaných do oddělení 200, 300 a 400 činí 100 000 USD, bude vytvořen jeden počáteční zůstatek pro pozdržené příjmy – 100. Vyberete-li možnost **Zavřít jedno** a ponecháte pole pro hodnotu finanční dimenze prázdné, všechny transakce se zaúčtují do pozdržených příjmů, přičemž tato hodnota dimenze nebude zadána. 

Proces roční uzávěrky neodpovídá účetním strukturám. Důvodem je skutečnost, že účetní struktury se mohou změnit během fiskálního roku a z důvodu těchto změn není vždy možné identifikovat příslušnou účetní strukturu.  Při vytváření počátečních transakcí budou zůstatky posunuty dopředu s finančními dimenzemi, jak to je definováno v šabloně roční uzávěrky. Položky počátečních zůstatků mohou zahrnovat finanční dimenze, které již nejsou v aktuální účetní struktuře, a kombinace segmentů, které již nejsou platné v aktuální účetní struktuře. Pokud vaše organizace chce vyloučit finanční dimenzi pro počáteční zůstatek pozdržených příjmů, nastavte finanční dimenzi na hodnotu **Zavřít jedno** a ponechejte pole hodnoty dimenze prázdné.

## <a name="run-the-year-end-close-process"></a>Spuštění procesu roční uzávěrky
Po vytvoření šablon roční uzávěrky je možné proces roční uzávěrky zahájit zvolením možnosti **Uzavřít fiskální rok** v podokně akcí. Vyberte buď všechny právnické osoby, nebo jejich podmnožinu ze šablony, pro kterou chcete roční uzávěrku spustit. Při spuštění roční uzávěrky v určitém fiskálním roce poprvé pravděpodobně zvolíte všechny právnické osoby, k vytvoření počátečních zůstatků pro všechny právnické osoby. Pokud budete spouštět roční uzávěrku znovu, můžete proces spustit pouze pro právnické osoby, pro které byly zaúčtovány položky úprav. 

Vyberte fiskální rok, pro který chcete proces roční uzávěrky spustit. Pokud existuje více období uzávěrky pro poslední období fiskálního roku, pole **Název období** bude k dispozici, abyste mohli vybrat, které období uzávěrky má zaúčtovat uzávěrkovou transakci, jestliže je v nastavení určeno, že se má vytvořit uzávěrková transakce. 

Zadejte číslo dokladu, které může nebo nemusí být vyžadováno, což záleží na nastavení v části Parametry hlavní knihy. Stejné číslo dokladu se použije pro všechny právnické osoby vybrané pro proces roční uzávěrky. Číslo dokladu se negeneruje pomocí číselné řady. Doporučuje se zadat číslo dokladu, i když není vyžadováno. Zadání čísla dokladu usnadňuje hledání počátečních transakcí v novém fiskálním roce. Pokud číslo dokladu nezadáte, doklad bude pro počáteční transakci prázdný. 

Pokud chcete stornovat předchozí roční uzávěrku pro vybraný fiskální rok, nastavte možnost **Vrátit zpět předchozí uzávěrku** na hodnotu **Ano**. Roční uzávěrka bude stornována, ale proces je možné kdykoli znovu spustit. Pokud stornujete nějakou roční uzávěrku, možnost **Datum poslední roční uzávěrky** nebude k dispozici. 

Proces roční uzávěrky se spustí ve výchozím dávkovém režimu. Spuštění procesu v dávkovém režimu je doporučený postup, umožní totiž uživateli návrat k jiným činnostem. Po dokončení procesu roční uzávěrky se aktualizuje pole **Datum poslední roční uzávěrky** za použití data relace.

Další informace naleznete v tématu [Uzavření hlavní knihy na konci obdob](close-general-ledger-at-period-end.md) a [Uzavření fiskálního roku](tasks/close-fiscal-year.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]