---
title: Přehled poradce při optimalizaci
description: Toto téma popisuje, jak můžete použít poradce při optimalizaci pro zajištění optimální konfigurace Finance and Operations.
author: roxanadiaconu
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SelfHealingWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: sericks
ms.search.validFrom: 2017-12-01
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 1e53dbae2d139af554b1918102937f8c3579f64a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682530"
---
# <a name="optimization-advisor-overview"></a>Přehled poradce při optimalizaci

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak můžete použít poradce při optimalizaci pro zajištění optimální konfigurace Finance and Operations.

## <a name="overview"></a>Přehled

Dostupnost funkcí v aplikaci, výkon systému a hladký průběh obchodních procesů může negativně ovlivnit nesprávná konfigurace a nastavení modulu. Kvalita obchodních údajů (například správnost, úplnost a čistota dat) také ovlivňuje výkonnost systému, stejně jako rozhodovací schopnosti organizace, produktivitu atd.

Pracovní prostor **Poradce při optimalizaci** je nástroj, který umožňuje uživatelům power user, obchodním analytikům, funkčním konzultantům a funkcím IT podpory identifikovat problémy v konfiguraci modulu a obchodních datech. Poradce při optimalizaci navrhuje doporučené postupy pro konfiguraci a identifikuje obchodní údaje, které jsou zastaralé nebo chybné.

Poradce při optimalizaci pravidelně spouští sadu pravidel doporučených postupů. K dispozici je výchozí sada pravidel, uživatelé však mohou vytvářet také pravidla, která jsou specifická pro svá vlastní nastavení, řešení od nezávislých dodavatelů softwaru (ISV) a o zaměstnání. Další informace o tom, jak vytvářet pravidla, naleznete v tématu [Vytvoření pravidel pro poradce optimalizací](./create-rules-optimization-advisor.md).

Při zjištění narušení pravidla se vygeneruje příležitost optimalizace a zobrazí se v pracovním prostoru **Poradce při optimalizaci**. Uživatel může provést odpovídající opravnou akci přímo z pracovního prostoru **poradce pro optimalizaci**.

Příležitosti mohou být specifické pro společnost nebo mezi různými společnostmi, v závislosti na typu nastavení a ověřovaných dat. Příležitosti mezi více společnostmi lze zobrazit ze všech společností. Chcete-li zobrazit příležitosti pro určitou společnost, musíte nejprve vybrat společnost.

Na příležitosti optimalizace se vztahují standardní zásady zabezpečení. Například příležitosti optimalizace, které souvisejí s konfigurací modulu **řízení skladu**, jsou zobrazeny pouze pro uživatele, kteří mají přístup k řízení skladu a mohou změnit jeho nastavení.

Pokud provedete akci týkající se některých možností optimalizace, systém vypočítá dopad příležitosti z hlediska snížení času spuštění obchodních procesů. Bohužel tato funkce není dostupná pro všechny příležitosti optimalizace.

Další informace o poradci při optimalizaci naleznete v krátkém videu [Poradce při optimalizaci v Dynamics 365 for Finance and Operations](https://www.youtube.com/watch?v=MRsAzgFCUSQ).

## <a name="optimization-rules"></a>Pravidla optimalizace

Chcete-li zobrazit úplný seznam pravidel poradce při optimalizaci a zjistit, jak často jsou pravidla vyhodnocována, přejděte na **Správa systému** &gt; **Pravidelné úlohy** &gt; **Udržovat pravidlo ověření diagnostiky**. Jsou vyhodnocována pouze pravidla, která se nacházejí ve stavu **Aktivní**. Četnost hodnocení lze nastavit na **Denní**, **Týdenní**, **Měsíční**, nebo **Nenaplánováno**.

Chcete-li spustit hodnocení neplánovaných pravidel nebo přehodnotit periodická pravidla mimo jejich určený plán, přejděte na **Správa systému** &gt; **Pravidelné úlohy** &gt; **Naplánovat pravidlo ověření diagnostiky**. Potom zvolte v dialogovém okně **Ověření pravidla diagnostiky** frekvenci vyhodnocení. Znovu se vyhodnotí všechna pravidla, která mají zadaný interval.

Aktuální sada pravidel optimalizace může být rozdělena do následujících kategorií.

### <a name="module-configuration-and-setup"></a>Konfigurace a nastavení modulu

Nastavení správy skladu je složitý proces. K usnadnění procesu byla zavedena některá pravidla umožňující ověřit správnost nastavení. Jedno pravidlo například ověřuje nastavení směrnice skladového místa pro pevné produkt varianty umístění pro prodejní objednávky a převodní příkazy.

Dále některá pravidla kontrolují, zda jsou skutečně použity funkce, které byly povoleny. Například jedno pravidlo určuje, zda chcete používat modul **hlavní plánování**. Pokud pravidlo určuje, zda nepoužíváte modul, je generována příležitost optimalizace navrhující, abyste procesy plánování vypli.

### <a name="system-configuration"></a>Konfigurace systému

Pokud není použita konkrétní funkce, která je řízena konfiguračním klíčem, je generována příležitost optimalizace naznačující, abyste zakázali konfigurační klíč. Příklady konfiguračních klíčů: **Skutečná hmotnost**, **Plánování rozpočtu**, **Projektu** a **Seznam schválených dodavatelů**.

### <a name="business-data-consistency-and-cleanup"></a>Konzistence a čištění obchodních dat

Pokud nejsou hlavní data správná (například v případě, že máte převody měrné jednotky pro jednotky, které nebyly definovány nebo pokud máte převody měrné jednotky s dělením 0 \[nula\]), je generována příležitost optimalizace k návrhu opravy údajů. 

Jestliže máte příliš mnoho položek historie dávkové úlohy, zastaralých položek, uzavřených položek na skladě povolených pro sklad položky a tak dále, nebo pokud jsou tyto položky zastaralé, budou moci navrhnout vyčištění dat. Tím, že budete udržovat data přehledná, můžete vylepšit celkový výkon systému.

### <a name="best-practices"></a>Doporučené postupy

Pokud nepoužíváte některé obchodní procesy podle doporučených postupů (například, když spustíte uzávěrku skladu před uzavřením skladu nebo plánovaný dávkový převod dílčí hlavní knihy dávky), příležitosti optimalizace vás budou informovat o nejlepším postupu a vyzve vás k jeho dodržování.

## <a name="optimization-opportunities"></a>Příležitosti optimalizace

Chcete-li zobrazit příležitosti optimalizace, které jsou generovány během vyhodnocení pravidel optimalizace, otevřete pracovní prostor **Poradce při optimalizaci**.

V tomto pracovním prostoru lze zobrazit další informace o příležitosti výběrem **Další informace**. Jestliže má systém provést akci a opravit nastavení, vyčistěte data a tak dále tak, abyste nemuseli otevírat odpovídající stránky sami, vyberte **provést akci**.

Neexistuje žádné workflow pro příležitosti optimalizace. Po výběru možnosti **Provést akci** nebo použití navigační cesty, která je k dispozici v dialogovém okně **Další informace** je příležitost optimalizace odebrána ze seznamu. Pokud opravná akce problém zcela nevyřeší, příležitost bude vygenerována znovu při dalším vyhodnocení tohoto pravidla.

Jestli se možnost nevztahuje na vaši roli, můžete vybrat **skrýt z mého seznamu**. I v případě, že pravidlo za tuto příležitost je spuštěno později, se nezobrazí příležitosti v tomto seznamu.

Chcete-li deaktivovat vyhodnocení konkrétních pravidel, zvolte příležitost vygenerovanou pravidlem a poté zvolte **Deaktivovat analýzy**.

## <a name="additional-resources"></a>Další zdroje

[Vytvoření pravidel pro poradce při optimalizaci](./create-rules-optimization-advisor.md)

[Poradce při optimalizaci v Dynamics 365 for Finance and Operations (Video)](https://www.youtube.com/watch?v=MRsAzgFCUSQ)
