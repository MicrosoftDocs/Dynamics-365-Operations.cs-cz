---
title: "Doporučené postupy pro import dokladů pomocí finančního deníku entity"
description: "Toto téma obsahuje tipy pro import dat do finančního deníku pomocí finančního deníku entity."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 94363
ms.assetid: 0b8149b5-32c5-4518-9ebd-09c9fd7f4cfc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 81a52acd1d9baa12fcfe9d848441901894fa5682
ms.lasthandoff: 03/31/2017


---

# <a name="best-practices-for-importing-vouchers-using-the-general-journal-entity"></a>Doporučené postupy pro import dokladů pomocí finančního deníku entity

[!include[banner](../includes/banner.md)]


Toto téma obsahuje tipy pro import dat do finančního deníku pomocí finančního deníku entity.  

Finanční deník entity lze importovat doklady, které mají typ účtu účet nebo posun o **kniha, zákazníka, dodavatele nebo bankovní**. Doklad lze zadat jako jeden řádek, použití obojího **účtu** pole a **protiúčet** pole, nebo jako více řádků dokladu, kde je pouze **účtu** pole se používá (a **protiúčet** je na každém řádku prázdné). Finančního deníku entity nepodporuje všechny typy účtů. Místo toho jsou k dispozici jiné entity pro scénáře, kde jsou vyžadovány různé kombinace typů účtů. Chcete-li importovat transakce projektu, například pomocí entity deníku výdajů projektu. Každá entita je navržen pro podporu konkrétní scénáře, což znamená, že další pole mohou být k dispozici v entitách u scénářů, ale ne v entity pro různé scénáře.

## <a name="setup"></a>Nastavení
Před importem pomocí finančního deníku entity ověřte následující nastavení:

-   **Nastavení číselné řady pro číslo dávky deníku** – ve výchozím nastavení při importu pomocí finančního deníku entity, používá číslo dávky deníku číselnou řadu, která je definována v parametrech hlavní knihy. Pokud nastavíte číselnou řadu pro číslo dávky deníku na **Ručně**, nebude použita výchozí hodnota. Toto nastavení není podporováno.
-   **Konfigurace finanční dimenze** -každá organizace musí definovat pořadí finančních dimenzí při entity slouží k importu transakcí. Je definováno pořadí **knihy dimenze integrace** formátu, na **financí**&gt;**účtové osnovy**&gt;**rozměry**&gt;**konfigurace finanční dimenze pro integraci aplikací**&gt;**vyberte entity data**. Segmenty účtu hlavní knihy, který je importován, musí mít stejné pořadí. Jinak dojde během importu k chybě.

## <a name="general-journal-entity-setup"></a>Nastavení entity obecného deníku
Dvě nastavení správy dat ovlivňuje způsob aplikování výchozí číslo dávky deníku nebo číslo dokladu:

-   **Zpracování na sadu** (u data entity)
-   **Automaticky generované** (na mapování polí)

Následující oddíly popisují účinek těchto nastavení, a také vysvětlují způsob, jakým se generují čísla dávky deníku a čísla dokladu.

### <a name="journal-batch-number"></a>Číslo dávky deníku

-   Nastavení **Zpracování založené na sadě** u entity obecného deníku neovlivňuje způsob, jakým jsou generovány čísla dávek deníku.
-   Pokud je pole **Číslo dávky deníku** nastaveno na **Automaticky generované**, nové číslo dávky deníku je vytvořeno pro každý řádek, který je importován. Toto chování není vhodné. Nastavení **Automaticky generované** se nachází u projektu importu v nabídce **Zobrazit mapu** na kartě **Podrobnosti mapování**.
-   Pokud není pole **Číslo dávky deníku** nastaveno na **Automaticky generované**, číslo dávky deníku je vytvořeno následovně:
    -   Pokud číslo dávky deníku, který je definován v importovaném souboru shoduje existující, nezaúčtované denního deníku 365 Microsoft Dynamics pro operace, jsou importovány všechny řádky, které mají odpovídající číslo dávky deníku do deníku. Řádky nejsou importovány do zaúčtovaného čísla dávky deníku. Místo toho je vytvořeno nové číslo.
    -   Pokud je číslo dávky deníku, který je definován v importovaném souboru neodpovídá existující, nezaúčtované denní deník v 365 Dynamics pro operace, všechny řádky, které mají stejné číslo dávky deníku jsou seskupeny pod do nového deníku. Například všechny řádky, které mají číslo dávky deníku 1, jsou importovány do nového deníku, a všechny řádky, které mají číslo dávky deníku 2, jsou importovány do druhého nového deníku. Číslo dávky deníku je vytvořeno pomocí číselné řady, která je definována v parametrech hlavní knihy.

### <a name="voucher-number"></a>Číslo dokladu

-   Při použití nastavení **Zpracování založené na sadě** u entitu obecného deníku je třeba uvádět číslo dokladu do importovaného souboru. Každá transakci ve finančním deníku je přiřazeno číslo dokladu, které je uvedeny v importovaném souboru, a to i v případě, že doklad není vyrovnán. Pokud chcete použít zpracování na sadu, ale chcete také použít číselnou řadu, která je definována pro čísla dokladů v 365 Dynamics pro operace, má k dispozici oprava hotfix pro vydání únor 2016. Číslo opravy hotfix je 3170316 a je k dispozici ke stažení na webu Lifecycle services (LCS). Další informace naleznete v tématu [Stažení oprav hotfix z webu Lifecycle Services](..\migration-upgrade\download-hotfix-lcs.md).
    -   Chcete-li povolit tuto funkci v názvu deníku, který se používá pro dovozy 365 Dynamics pro operace, nastavte **číslo přidělení při zaúčtování** k **Ano**.
    -   Číslo dokladu musí být i přesto definováno v importovaném souboru. Toto číslo však je dočasný a přepsán 365 Dynamics pro operace číslo dokladu při zaúčtování deníku. Ujistěte se, že řádky deníku jsou seskupeny správně podle dočasného čísla dokladu. Například při zaúčtování tři řádky jsou nalezeno dočasný doklad číslo 1. Číslo dokladu pro dočasný všech tří řádků je přepsán dalším číslem v číselné řadě. Nejsou-li tyto tři řádky vyrovnané entity, doklad nebude zaúčtován. Dále v případě nalezení řádků, které mají dočasné číslo dokladu 2, je toto číslo přepsáno dalším číslem dokladu v číselné řadě, atd.

<!-- -->

-   Pokud nepoužíváte **zpracování sadu na** nastavení, ne musíte zadat číslo dokladu v importovaném souboru. Čísla dokladů jsou vytvořena během importu na základě nastavení názvu deníku (**Pouze jeden doklad**, **Ve spojení s zůstatkem** a tak dále). Například, pokud je definován název deníku jako **Ve spojení s zůstatkem**, první řádek obdrží nové výchozí číslo dokladu. Systém vyhodnocuje řádek s cílem určit, zda se strana Dáti rovná straně Dal. Pokud existuje protiúčet na řádku, další řádek, který je importován, obdrží nové číslo dokladu. Pokud neexistuje žádný protiúčet, systém vyhodnotí, zda se strana Dáti rovná straně Dal, vždy, když je importován nový řádek.
-   Pokud je pole **Číslo dokladu** nastaveno na **Automaticky generované**, import se nezdaří. Nastavení **Automaticky generované** pro pole **Číslo dokladu** není podporováno.

Ve výchozím nastavení používají entity obecného deníku zpracování založené na sadě. Po vyhodnocení obchodních požadavků vaší organizace můžete změnit nastavení **Zpracování založené na sadě** klepnutím na **Datové entity** v pracovním prostoru **Správa dat**. Zpracování založené na sadě se používá k urychlení procesu importu. Pokud nechcete zpracování založené na sadě použít, import entity obecného deníku bude pomalejší.




