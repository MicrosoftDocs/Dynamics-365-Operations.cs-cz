--- 
title: "Výběr definic datového modelu při vytváření formátů"
description: "K provedení kroků v tomto postupu musíte nejprve dokončit postup \"ER Vytvoření poskytovatele konfigurace a jeho označení jako aktivního\"."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: dc357db8acbdb98741a694a8a9d3c0c0625c50e4
ms.contentlocale: cs-cz
ms.lasthandoff: 08/08/2018

---
# <a name="select-data-model-definitions-when-you-create-formats"></a>Výběr definic datového modelu při vytváření formátů

[!include [task guide banner](../../includes/task-guide-banner.md)]

K provedení kroků v tomto postupu musíte nejprve dokončit postup "ER Vytvoření poskytovatele konfigurace a jeho označení jako aktivního". 

Tento postup popisuje, jak lze vybrat kořenovou položku modelu jako definici datového modelu pro vložení konfigurace nastavení elektronického vykazování (ER), které slouží ke generování elektronických dokumentů. V tomto postupu přidáte novou konfiguraci formátu ER pro vzorovou společnost Litware, Inc. 

Tento postup je navržen pro uživatele s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování. Kroky lze dokončit za použití libovolné datové sady.

1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
    * Ujistěte se, že poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako Aktivní. Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu „Vytvoření poskytovatele konfigurace a jeho označení jako aktivního“.  
2. Klikněte na Konfigurace výkaznictví.

## <a name="add-a-new-er-data-model-configuration"></a>Přidání nové konfigurace datového modelu ER
1. Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.
    * Doporučujeme přidat novou konfiguraci modelu ER, která obsahuje datový model, který je určen jako zdroj dat pro generování sestav ER.  
2. V poli Název zadejte Model platby (fiktivní).
    * Model platby (fiktivní)  
3. Klepněte na možnost Vytvořit konfiguraci.
4. Klikněte na možnost Návrhář.
    * Otevřete návrháře ER a určete strukturu datového modelu této konfigurace.  
    * Předpokládejme, že navrhneme datový model obchodní domény pro platby tak, aby podporovala 2 způsoby platby – bezhotovostní a přímý debet.  
5. Kliknutím na možnost Nový otevřete dialogové okno.
6. Do pole Název zadejte Platby – převedení kreditu.
    * Platby – převedení kreditu  
7. Klepněte na možnost Přidat.
8. Kliknutím na možnost Nový otevřete dialogové okno.
9. Do pole Nový uzel zadejte Kořen modelu.
10. Do pole Název zadejte Platby – přímý debet.
    * Platby – přímý debet  
11. Klepněte na možnost Přidat.
12. Klikněte na položku Uložit.
13. Zavřete stránku.
14. Klikněte na položku Změnit stav.
    * Dokončete pracovní verzi modelu a umožněte tak, aby byla k dispozici v mapování a formátech nového modelu.  
15. Klikněte na tlačítko Dokončit.
16. Klikněte na tlačítko OK.

## <a name="start-to-enter-a-new-er-format-configuration"></a>Začněte zadáním nové konfigurace formátu ER
1. Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.
2. V poli Nový zadejte Formát založený na datovém modelu Model platby (fiktivní).
3. V poli Definice datového modelu zadejte nebo vyberte hodnotu.
    * Všimněte si, že všechny kořenové položky vybraného datového modelu jsou aktuálně k dispozici pro výběr jako definice datového modelu. Můžete dále navrhovat formát pomocí některé z požadovaných kořenových položek datového modelu. Chybějící mapování modelu pro vybranou kořenovou položku vám nezabrání pokračovat.  
4. Zavřete stránku.

## <a name="add-a-new-er-model-mapping-configuration"></a>Přidání nové konfigurace mapování modelu ER
1. Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.
2. V poli Nový zadejte Mapování modelu založené na datovém modelu Model platby (fiktivní).
3. V poli Název zadejte Mapování modelu platby (fiktivní).
    * Mapování modelu platby (fiktivní)  
4. V poli Definice datového modelu zadejte nebo vyberte hodnotu.
5. Klepněte na možnost Vytvořit konfiguraci.

## <a name="design-er-model-mappings"></a>Navrhněte mapování modelu ER
1. Klikněte na možnost Návrhář.
    * Pomocí návrháře ER určete mapování modelu pro požadované kořenové položky.  
2. Klikněte na možnost Návrhář.
    * Simulujte nastavení vybraného mapování modelu pro kořenovou položku vybraného modelu.  
3. Ve stromové struktuře vyberte Dynamics 365 for Operations\Záznamy tabulky.
4. Klikněte na možnost Přidat kořen.
5. Do pole Název zadejte Hlavní kniha.
6. Do pole Tabulka zadejte hodnotu „LedgerJournalTrans“.
    * LedgerJournalTrans  
7. Klikněte na tlačítko OK.
8. Klikněte na položku Uložit.
9. Zavřete stránku.
10. Zavřete stránku.

## <a name="start-to-enter-another-new-er-format-configuration"></a>Začněte zadáním další nové konfigurace formátu ER
1. Ve stromovém zobrazení vyberte Model platby (fiktivní).
2. Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.
3. V poli Nový zadejte Formát založený na datovém modelu Model platby (fiktivní).
4. V poli Definice datového modelu zadejte nebo vyberte hodnotu.
    * Nyní je tak k dispozici k mapování zdrojů dat aplikace pouze jedna kořenová položka. Po uvedení alespoň jednoho modelu mapování jsou mapovány ke zdrojům dat aplikace pouze kořenové položky modelu, které lze vybrat jako definici modelu po přidání formátu ER.   
5. Zavřete stránku.


