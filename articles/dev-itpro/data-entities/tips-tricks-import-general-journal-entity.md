---
title: "Osvědčené postupy pro import dokladů pomocí entity obecného deníku"
description: "Toto téma obsahuje tipy pro import dat do finančního deníku pomocí entity obecného deníku."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 94363
ms.assetid: 0b8149b5-32c5-4518-9ebd-09c9fd7f4cfc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: a45a75d23c77af86b55866f99a97343a210ec777
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="best-practices-for-importing-vouchers-using-the-general-journal-entity"></a>Osvědčené postupy pro import dokladů pomocí entity obecného deníku

[!include[banner](../includes/banner.md)]


Toto téma obsahuje tipy pro import dat do finančního deníku pomocí entity obecného deníku.  

Entity obecného deníku lze použít pro import dokladů, které mají typ účtu nebo protiúčtu **Hlavní kniha, odběratel, dodavatel nebo banka**. Doklad lze zadat jako jeden řádek, pomocí pole **Účet** i **Protiúčet** nebo jako více řádků dokladu, kde je použito pouze pole **Účet** (a pole **Protiúčet** je na každém řádku prázdné). Entita finančního deníku nepodporuje všechny typy účtů. Místo toho jsou k dispozici jiné entity pro scénáře, kde jsou vyžadovány různé kombinace typů účtů. Chcete-li importovat transakce projektu, použijte entitu deníku výdajů projektu. Každá entita je navržena tak, aby podporovala konkrétní scénáře, což znamená, že další pole mohou být k dispozici pro scénáře entity, ale ne v entitách pro různé scénáře.

## <a name="setup"></a>Nastavení
Před importem pomocí entity obecného deníku ověřte následující nastavení:

-   **Nastavení číselné řady pro číslo dávky deníku** – ve výchozím nastavení při importu pomocí entity obecného deníku používá číslo dávky deníku číselnou řadu, která je definována v parametrech hlavní knihy. Pokud nastavíte číselnou řadu pro číslo dávky deníku na **Ručně**, nebude použita výchozí hodnota. Toto nastavení není podporováno.
-   **Konfigurace finanční dimenze** – každá organizace musí definovat pořadí finančních dimenzí, když entity slouží k importu transakcí. Pořadí je definováno pro formát **Integrace dimenzí hlavní knihy** v nabídce **hlavní kniha** &gt; **účtová osnova** &gt; **dimenze** &gt; **Konfigurace finanční dimenze pro integraci aplikací** &gt; **Výběr datových entit**. Segmenty účtu hlavní knihy, který je importován, musí mít stejné pořadí. Jinak dojde během importu k chybě.

## <a name="general-journal-entity-setup"></a>Nastavení entity obecného deníku
Dvě nastavení správy dat ovlivňují způsob aplikování výchozího čísla dávky deníku nebo čísla dokladu:

-   **Zpracování na základě sady** (u datové entity)
-   **Automaticky generované** (u mapování polí)

Následující oddíly popisují účinek těchto nastavení, a také vysvětlují způsob, jakým se generují čísla dávky deníku a čísla dokladu.

### <a name="journal-batch-number"></a>Číslo dávky deníku

-   Nastavení **Zpracování založené na sadě** u entity obecného deníku neovlivňuje způsob, jakým jsou generovány čísla dávek deníku.
-   Pokud je pole **Číslo dávky deníku** nastaveno na **Automaticky generované**, nové číslo dávky deníku je vytvořeno pro každý řádek, který je importován. Toto chování není vhodné. Nastavení **Automaticky generované** se nachází u projektu importu v nabídce **Zobrazit mapu** na kartě **Podrobnosti mapování**.
-   Pokud není pole **Číslo dávky deníku** nastaveno na **Automaticky generované**, číslo dávky deníku je vytvořeno následovně:
    -   Pokud číslo dávky deníku, který je definován v importovaném souboru, odpovídá existujícímu, nezaúčtovanému dennímu deník, jsou všechny řádky, které mají odpovídající číslo dávky deníku, importovány do existujícího deníku. Řádky nejsou importovány do zaúčtovaného čísla dávky deníku. Místo toho je vytvořeno nové číslo.
    -   Pokud číslo dávky deníku, který je definován v importovaném souboru, neodpovídá existujícímu, nezaúčtovanému dennímu deníku, jsou všechny řádky, které mají stejné číslo dávky deníku, seskupeny v novém deníku. Například všechny řádky, které mají číslo dávky deníku 1, jsou importovány do nového deníku, a všechny řádky, které mají číslo dávky deníku 2, jsou importovány do druhého nového deníku. Číslo dávky deníku je vytvořeno pomocí číselné řady, která je definována v parametrech hlavní knihy.

### <a name="voucher-number"></a>Číslo dokladu

-   Při použití nastavení **Zpracování založené na sadě** u entitu obecného deníku je třeba uvádět číslo dokladu do importovaného souboru. Každá transakci ve finančním deníku je přiřazeno číslo dokladu, které je uvedeny v importovaném souboru, a to i v případě, že doklad není vyrovnán. Pokud chcete použít zpracování založené na sadě, ale chcete také použít číselnou řadu, která je definována pro čísla dokladů, byla vytvořena oprava hotfix pro verzi z února 2016. Číslo opravy hotfix je 3170316 a je k dispozici ke stažení na webu Lifecycle services (LCS). Další informace naleznete v tématu [Stažení oprav hotfix z webu Lifecycle Services](..\migration-upgrade\download-hotfix-lcs.md).
    -   Chcete-li povolit tuto funkci, nastavte u názvu deníku, který se používá pro import, na možnost **Přidělení čísla při zaúčtování** na **Ano**.
    -   Číslo dokladu musí být i přesto definováno v importovaném souboru. Toto číslo však je dočasné a přepíše se čísel dokladu při zaúčtování deníku. Ujistěte se, že řádky deníku jsou seskupeny správně podle dočasného čísla dokladu. Například při zaúčtování jsou nalezeny tři řádky, které mají dočasný doklad číslo 1. Dočasné číslo dokladu pro všechny tři řádky je přepsáno dalším číslem v číselné řadě. Nejsou-li tyto tři řádky vyrovnané entity, doklad nebude zaúčtován. Dále v případě nalezení řádků, které mají dočasné číslo dokladu 2, je toto číslo přepsáno dalším číslem dokladu v číselné řadě, atd.

<!-- -->

-   Pokud nepoužijete nastavení **Zpracování založené na sadě**, není třeba uvádět číslo dokladu v importovaném souboru. Čísla dokladů jsou vytvořena během importu na základě nastavení názvu deníku (**Pouze jeden doklad**, **Ve spojení s zůstatkem** a tak dále). Například, pokud je definován název deníku jako **Ve spojení s zůstatkem**, první řádek obdrží nové výchozí číslo dokladu. Systém vyhodnocuje řádek s cílem určit, zda se strana Dáti rovná straně Dal. Pokud existuje protiúčet na řádku, další řádek, který je importován, obdrží nové číslo dokladu. Pokud neexistuje žádný protiúčet, systém vyhodnotí, zda se strana Dáti rovná straně Dal, vždy, když je importován nový řádek.
-   Pokud je pole **Číslo dokladu** nastaveno na **Automaticky generované**, import se nezdaří. Nastavení **Automaticky generované** pro pole **Číslo dokladu** není podporováno.

Ve výchozím nastavení používají entity obecného deníku zpracování založené na sadě. Po vyhodnocení obchodních požadavků vaší organizace můžete změnit nastavení **Zpracování založené na sadě** klepnutím na **Datové entity** v pracovním prostoru **Správa dat**. Zpracování založené na sadě se používá k urychlení procesu importu. Pokud nechcete zpracování založené na sadě použít, import entity obecného deníku bude pomalejší.




