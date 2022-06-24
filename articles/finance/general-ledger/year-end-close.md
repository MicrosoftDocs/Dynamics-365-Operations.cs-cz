---
title: Roční uzávěrka
description: Tento článek popisuje požadované nastavení a postup pro spuštění procesu roční uzávěrky hlavní knihy.
author: kweekley
ms.date: 12/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: kfend
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 032c572ec7b29bb6b2823ddde0c4fa76e5f8fcf1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883206"
---
# <a name="year-end-close"></a>Roční uzávěrka

[!include [banner](../includes/banner.md)]

Tento článek popisuje požadované nastavení a postup pro spuštění procesu roční uzávěrky hlavní knihy.

Na konci fiskálního roku je nutné spustit proces roční uzávěrky k převodu počátečních zůstatků do nového roku. Většina organizací spouští proces roční uzávěrky několikrát. První běh přesune zůstatky do nového fiskálního roku. Proces lze potom spustit znovu, a to tolikrát, kolikrát je třeba, a přesunout zůstatky z položek úprav do nového fiskálního roku.

Během procesu roční uzávěrky mohou být vytvořeny dva typy možných transakcí. Počáteční transakce je vždy vygenerována a slouží k vytváření počátečních zůstatků v novém fiskálním roce. Počáteční transakce zobrazí zůstatky účtů rozvahového účtu v novém fiskálním roce a zůstatky ze zůstatků účtu hlavní knihy zisků a ztrát na účtu hlavní knihy pozdržených příjmů v novém fiskálním roce. Uzávěrková transakce je vytvořena volitelně, aby bylo možné uvést zůstatky účtů zisků a ztrát na nulu ve fiskálním roce, který je uzavírán.

## <a name="prepare-to-run-the-year-end-close"></a>Příprava ke spuštění roční uzávěrky

Před spuštěním procesu roční uzávěrky ověřte následující nastavení:

Na stránce **Hlavní účet** proveďte toto:

- Ověřte, že je pole **Typ hlavního účtu** správně nastaveno pro každý hlavní účet. Typ hlavního účtu se určuje, zda zůstatek hlavního účtu bude posunut dopředu jako počáteční zůstatek nebo uzavřen v pozdržených příjmech v počáteční transakci.
- Zůstatek hlavního účtu lze převést do nového hlavního účtu během roční uzávěrky. Zadejte nový hlavní účet do pole **Počáteční účet**. Obvykle se toto pole používá pro rozvahové hlavní účty, když je hlavní účet deaktivován a nový hlavní účet se používá pro nový fiskální rok.

Na stránce **Parametry hlavní knihy** pod položkou **Uzávěrka fiskálního roku**:

- Možnost **Odstranit stávající položky roční uzávěrky při opakování roční uzávěrky** se používá k určení, zda počáteční transakce generovaná systémem z předchozí roční uzávěrky má být odstraněna, když je roční uzávěrka spuštěna znovu. Pokud je tato možnost nastavena na hodnotu **Ano**, předchozí počáteční a volitelné uzávěrkové transakce jsou odstraněny a nová počáteční nebo uzávěrková transakce se vytvoří na základě aktuálních zůstatků. Pokud je tato možnost nastavena na hodnotu **Ne**, předchozí počáteční a volitelné uzávěrkové transakce jsou zachovány a vytvoří se další počáteční nebo uzávěrkové transakce k přesunutí zůstatků dopředu z transakcí úprav zaúčtovaných po předchozí roční uzávěrce.
- Možnost **Vytvořit uzávěrkové transakce při převodu** se používá k vytvoření uzávěrkových transakcí ve fiskálním roku, který je uzavírán, aby zůstatky všech hlavních účtů mohly vykazovat 0 (nulu). Pokud je tato možnost nastavena na **Ano**, je vytvořena jak počáteční transakce, tak i uzávěrková transakce. Pokud je tato možnost nastavena na **Ne**, je vytvořena pouze počáteční transakce v dalším fiskálním roku k převodu zůstatků. Zůstatky hlavního účtu zůstávají na konci fiskálního roku.
- Možnost **Nastavit stav fiskálního roku na trvale uzavřený** slouží k nastavení stavu fiskálního roku „trvale uzavřený“. Tuto možnost používejte opatrně, protože období, která mají trvale uzavřený stav, nelze znovu otevřít. Proto úpravy nelze zaúčtovat do fiskálního roku. Je doporučeno tuto možnost nastavit na hodnotu **Ne**.
- Možnost **Je nutné vyplnit číslo dokladu** byla odstraněna. Když je spuštěn proces roční uzávěrky, je nyní vyžadován doklad. V té době se číslo dokladu zadává ručně.

Na stránce **Fiskální kalendář**:

- Příští fiskální rok musí existovat před spuštěním roční uzávěrky. Jinak nelze počáteční zůstatky v úvodním období vytvořit.

Na stránce **Kalendář hlavní knihy**:

- Volitelné: Jednotlivá fiskální období pro fiskální rok, který je uzavírán, lze nastavit na hodnotu **Blokováno**, chcete-li zabránit v zadávání nových transakcí. Při zjištění položek úprav lze znovu otevřít blokovaná období a zaúčtovat položky úprav, a to i v případě, že již byl spuštěn proces roční uzávěrky.

Na stránce **Nastavení šablony roční uzávěrky**.

- Pokud je funkce **Vylepšení roční uzávěrky hlavní knihy** zapnutá, proces nastavení šablony roční uzávěrky je oddělen od procesu spouštění roční uzávěrky. Šablonu lze definovat na stránce **Nastavení šablony roční uzávěrky** (**Hlavní kniha \> Nastavení hlavní knihy \> Nastavení šablony roční uzávěrky**) nebo k němu lze přistupovat z procesu roční uzávěrky.

## <a name="define-year-end-close-templates"></a>Definování šablon roční uzávěrky

Po konfiguraci systému můžete spustit proces roční uzávěrky. Na stránce **Nastavení šablony roční uzávěrky** lze definovat šablonu pro skupinu právnických osob, pro kterou bude roční uzávěrka spuštěna. Tato šablona se znovu použije u každé roční uzávěrky, při změně v organizaci již však lze upravit.

Nejprve nastavte pole **Název skupiny** pro šablonu a vyberte fiskální kalendář. Název skupiny by měl označovat skupinu zahrnutých právnických osob. Když určujete skupiny právnických osob, nezapomeňte, že právnické osoby lze zahrnout do stejné skupiny, pouze pokud je pro ně vybrán stejný fiskální kalendář. Například šablona může být nastavena na základě zeměpisné polohy a může zahrnovat samostatné skupiny vytvořené pro právnické osoby Severní Ameriky, právnické osoby zemí Evropy, Středního východu a Afriky (EMEA) a právnické osoby zemí Asie a Pacifiku (APAC).

Potom lze tyto právnické osoby přidat do šablony. Právnické osoby lze přidat zvolením organizační hierarchie nebo právnických osob. Pokud je vybrána organizační hierarchie, do šablony budou přidány pouze právnické osoby v rámci hierarchie, která používá vybraný fiskální kalendář. Při přidávání právnických osob do šablony mohou být přidány pouze právnické osoby se stejným fiskálním kalendářem. Stejný fiskální kalendář je vyžadován, protože se roční uzávěrka spouští zvolením fiskálního roku, který se může kalendář od kalendáře lišit.

Po přidání právnických osob se definujte hlavní účty pozdržených příjmů pro každou právnickou osobu.

Karta **Finanční dimenze** slouží k definování, které finanční dimenze budou použity v počáteční transakci. Nastavení, která definujete, se týkají pouze právnické osoby vybrané v mřížce **Právnické osoby**. Toto nastavení zopakujete pro každou právnickou osobu v mřížce.

Možnost **Převést dimenze rozvahy** slouží ke specifikaci, zda finanční dimenze v transakcích zaúčtovaných na rozvahové účty mají být spravovány v počáteční transakci. Je doporučeno tuto možnost nastavit na hodnotu **Ano**. Nastavení dimenzí rozvahy neovlivní existující zůstatky v účtech hlavní knihy nerozděleného zisku. Tyto zůstatky jsou určeny dimenzemi zisků a ztrát, které jsou definovány v další části. Například fiskální rok 2019 byl prvním rokem, který byl uzavřen, amožnost **Zavřít vše** byla použita k výběru dimenzí **Oddělení** a **Nákladové středisko** pro uzávěrku. V tomto případě byl pro každou kombinaci oddělení a nákladového střediska vytvořen samostatný účet nerozděleného zisku. Když je spuštěna roční uzávěrka pro fiskální rok 2020, nerozdělený zisk z předchozího roku zůstává přesně tak, jak byl zaúčtován, i když je možnost **Přenést dimenze rozvahy** nastavena na **Ne**. Zůstatky, které jsou zaúčtovány do nerozděleného zisku z uzávěrek z předchozího roku, se nikdy nezmění.

Sekce **Převést dimenze zisků a ztrát** slouží k definování, které finanční dimenze v transakcích zaúčtovaných na účtu zisků a ztrát budou převedeny do hlavního účtu pozdržených příjmů. Nejprve určete finanční dimenze, které jsou relevantní pro vybranou právnickou osobu. Tyto finanční dimenze zahrnují všechny finanční dimenze zaúčtované v daném roce i v případě, že finanční dimenze není součástí aktivní účetní struktury. Dále určete každou dimenzi jako **Zavřít jedno** nebo **Uzavřít vše**. Výchozí volbou je **Uzavřít vše**. Tato možnost udržuje původní hodnoty finanční dimenze ze zaúčtovaných transakcí a používá je pro vytvoření počátečních zůstatků pro účet pozdržených příjmů. Vytvoří se samostatné počáteční zůstatky pozdržených příjmů pro každou jedinečnou kombinaci hodnot finančních dimenzí. Pokud je zvolena možnost **Zavřít jedno**, všechny transakce zaúčtované s touto finanční dimenzí budou shrnuty do počátečního zůstatku pozdržených příjmů pro hodnotu dimenze zadanou v poli po **Zavřít jedno**. Například s účetní strukturou **Hlavní účet – oddělení** byly zaúčtovány všechny transakce pro daný fiskální rok. Ve finanční dimenzi **oddělení** v šabloně je vybrána možnost **Zavřít jedno** a je zadána hodnota **100** coby hodnota dimenze. Pokud celkový příjem u všech transakcí zaúčtovaných do oddělení 200, 300 a 400 činí 100 000 USD, bude vytvořen jeden počáteční zůstatek pro **Pozdržené příjmy – 100**. Vyberete-li možnost **Zavřít jedno**, avšak ponecháte pole pro hodnotu finanční dimenze prázdné, všechny transakce se zaúčtují do pozdržených příjmů, přičemž tato hodnota dimenze nebude zadána.

## <a name="run-the-year-end-close-process"></a>Spuštění procesu roční uzávěrky

Po vytvoření šablon roční uzávěrky můžete zahájit proces roční uzávěrky na stránce **Roční uzávěrka** (**Hlavní kniha \> Uzavření období \> Roční uzávěrka**). Před spuštěním roční uzávěrky můžete přidat nové šablony roční uzávěrky nebo upravit existující šablony výběrem **Nastavení šablony roční uzávěrky** pro otevření stránky nastavení šablon.

Vyberte šablonu roční uzávěrky a poté v podokně akcí vyberte **Spustit roční uzávěrku**. Vyberte buď všechny právnické osoby, nebo jejich podmnožinu ze šablony, pro kterou chcete roční uzávěrku spustit. Při spuštění roční uzávěrky v určitém fiskálním roce poprvé pravděpodobně zvolíte všechny právnické osoby, k vytvoření počátečních zůstatků pro všechny právnické osoby. Pokud jste již roční uzávěrku spouštěli, možná ji budete chtít spustit znovu pouze pro právnické osoby, pro které byly zaúčtovány položky úprav.

Dále vyberte fiskální rok, pro který chcete proces roční uzávěrky spustit. Pokud pro poslední období fiskálního roku existuje více než jedno závěrečné období, pole **Název období** bude k dispozici. Poté můžete vybrat období uzávěrky, které se použije k zaúčtování závěrečné transakce, pokud je definováno nastavení pro vytvoření závěrečné transakce.

Dále zadejte číslo dokladu. Stejné číslo dokladu se použije pro všechny právnické osoby vybrané pro proces roční uzávěrky. Číslo dokladu se negeneruje pomocí číselné řady.

Ve výchozím nastavení se proces roční uzávěrky spustí v dávkovém režimu. Po jejím zahájení se tedy můžete vrátit k dalším aktivitám.

Protože se struktury účtu mohou v průběhu fiskálního roku měnit, nelze vždy identifikovat příslušnou strukturu účtu. Proces roční uzávěrky tedy neodpovídá účetním strukturám. Při vytváření počátečních transakcí budou zůstatky posunuty dopředu s finančními dimenzemi, jak to je definováno v šabloně roční uzávěrky. Položky počátečních zůstatků mohou zahrnovat finanční dimenze, které již nejsou v aktuální účetní struktuře, a kombinace segmentů, které již nejsou platné v aktuální účetní struktuře. Pokud vaše organizace chce vyloučit finanční dimenzi pro počáteční zůstatek pozdržených příjmů, definujte finanční dimenzi na hodnotu **Zavřít jedno** a ponechejte pole hodnoty dimenze prázdné.

Po dokončení procesu se vytvoří záznam pro každou kombinaci právnické osoby a fiskálního roku. Budou se vám zobrazovat pouze záznamy týkající se právnických osob, ke kterým máte přístup. Každý záznam obsahuje systémové datum a čas, kdy byl proces spuštěn, a přímý odkaz na doklady, které byly vytvořeny pro roční uzávěrku.

[![Záznamy vytvořené na pevné záložce historie roční uzávěrky na stránce roční uzávěrky](./media/run-yr-end-close.png)](./media/run-yr-end-close.png)

Pokud znovu spustíte roční uzávěrku, uvidíte jeden nebo více záznamů pro každou kombinaci právnické osoby a fiskálního roku, v závislosti na nastavení možnosti **Při opětovné roční uzávěrce smažte existující položky roční uzávěrky** na stránce **Parametry hlavní knihy**:

- Pokud je možnost nastavena na **Ano**, dojde k odstranění dokladu předchozí roční uzávěrky. Záznam je označen jako **Stornován** a označen datem a časem, kdy bylo provedeno storno. Dále je odstraněn odkaz na číslo dokladu. Po dokončení roční uzávěrky se vytvoří nový záznam pro nový doklad, který se vytvoří.
- Pokud je možnost nastavena na **Ne**, zůstává záznam o roční uzávěrce z předchozího roku spolu s odkazem na doklad. Pokaždé, když je znovu spuštěna roční uzávěrka, bude vytvořen nový záznam spolu s odkazem na nové doklady.

## <a name="reverse-the-year-end-close-process"></a>Storno procesu roční uzávěrky

Na stránce **Roční uzávěrka** můžete provést storno roční uzávěrky. Vyberte záznam pro kombinaci právnické osoby a fiskálního roku, který musí být stornován, a poté vyberte **Storno roční uzávěrky**. Proces storna odstraní všechny počáteční a závěrečné doklady, které byly vytvořeny pro fiskální rok. Záznam je označen jako **Stornován** a označen datem a časem, kdy bylo provedeno storno. Dále je odstraněn odkaz na číslo dokladu. Stejně jako proces roční uzávěrky se storno spustí v dávkovém režimu.

Zaškrtávací políčko **Zobrazit stornované**, které je k dispozici nad mřížkou, umožňuje skrýt nebo zobrazit záznamy o stornovaných procesech roční uzávěrky. Po spuštění procesu **Storno roční uzávěrky** možná budete muset vybrat zaškrtávací políčko **Zobrazit stornované** pro zobrazení záznamu. Můžete nastavit další filtry pro zobrazení dalších informací.

[![Pomocí zaškrtávacího políčka Zobrazit stornované zobrazíte záznamy o stornovaných ročních uzávěrkách na stránce Roční uzávěrka](./media/rvrs-yr-end-close.png)](./media/rvrs-yr-end-close.png)

Další informace naleznete v tématu [Uzavření hlavní knihy na konci obdob](close-general-ledger-at-period-end.md) a [Uzavření fiskálního roku](tasks/close-fiscal-year.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
