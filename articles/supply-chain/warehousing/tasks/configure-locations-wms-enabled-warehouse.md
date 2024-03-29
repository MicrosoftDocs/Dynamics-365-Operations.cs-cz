---
title: Konfigurace umístění ve skladu s povolenými procesy řízení skladu
description: Tento průvodce popisuje konfiguraci skladového místa pro nový sklad WMS (sklad, který používá procesy správy skladu (WMS)).
author: perlynne
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, WHSLocationFormat, WHSLocationType, WHSLocationProfile, WHSParameters, WHSZoneGroup, WHSZone, WHSLocationBuild, WHSLocation, WHSPackSizeCategory, WHSLocationLimit, WHSInventFixedLocation, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4cce7ea0c06938d2ce038853a262f843ec76fe4c
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219651"
---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a>Konfigurace umístění ve skladu s povolenými procesy řízení skladu

[!include [banner](../../includes/banner.md)]

Tento průvodce popisuje konfiguraci skladového místa pro nový sklad WMS (sklad, který používá procesy správy skladu (WMS)). Proces obvykle provádějí vedoucí skladu. Tohoto průvodce můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat. Předpokladem je, že máte nakonfigurován alespoň jeden site.


## <a name="create-a-new-warehouse"></a>Vytvoření nového skladu
1. Přejděte na **Navigační podokno > Moduly > Řízení zásob > Nastavení > Rozdělení zásob > Sklady**.
2. Klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **Sklad**.
4. Zadejte hodnotu do pole **Název**.
5. V poli **Web** vyberte nebo zadejte existující hodnotu webu.
6. Rozbalte sekci **Sklad**.
7. Nastavte **Použít procesy řízení skladu** na Ano. Toto nastavení umožňuje spustit procesy správy skladu (WMS) prostřednictvím skladové práce a mobilních zařízení.
8. Zavřete stránku.

## <a name="define-a-location-format"></a>Definování formátu skladového místa
1. Přejděte na **Navigační podokno > Moduly > Řízení skladu > Nastavení > Sklad > Formáty umístění**. Formáty skladového místa představují systém pojmenování pro vytváření jedinečných a konzistentních názvů pro pozice přihrádky skladového místa používané ve skladu. Může být užitečný při použití oddělovačů ve formátu skladového místa pro usnadnění identifikace součástí skladového místa, například číslo uličky. V tomto příkladu vytvoříte název se čtyřmi součástmi. Může to být například ulička, stojan, police a přihrádka.
2. Klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **Formát umístění**.
4. Zadejte hodnotu do pole **Název**.
5. Zadejte hodnotu do pole **Popis segmentu**. Popisuje, co představuje první součást názvu skladového místa. Může to být například ‚Ulička‘.
6. Do pole **Délka** zadejte číslo. Určuje, kolik znaků musí mít tato část názvu skladového místa. Součet všech součástí v názvu, včetně oddělovačů, nesmí překročit 10 znaků.    
7. Zadejte hodnotu do pole **Oddělovač**. Určuje, jaký znak nebo symbol bude použit mezi první a druhou součástí názvu.  
8. V části **Podrobnosti** klikněte na **Nový**.
9. Zadejte hodnotu do pole **Popis segmentu**.
10. Do pole **Délka** zadejte číslo.
11. Zadejte hodnotu do pole **Oddělovač**.
12. V části **Podrobnosti** klikněte na **Nový**.
13. Zadejte hodnotu do pole **Popis segmentu**.
14. Do pole **Délka** zadejte číslo.
15. Zadejte hodnotu do pole **Oddělovač**.
16. V části **Podrobnosti** klikněte na **Nový**.
17. Zadejte hodnotu do pole **Popis segmentu**.
18. Do pole **Délka** zadejte číslo.
19. Klikněte na možnost **Uložit**.
20. Zavřete stránku.

## <a name="define-location-types"></a>Definování typů skladových míst
1. Přejděte na **Navigační podokno > Moduly > Řízení skladu > Nastavení > Sklad > Typy umístění**. Typy skladových míst lze použít jako možnosti filtrování k řízení různých procesů správy skladu. Minimální podmínkou pro možnost definování procesu správy výstupního skladu je vytvoření typů přechodných a konečných skladových míst. 
2. Klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **Typ místa**.
4. Zadejte hodnotu do pole **Popis**.
5. Zavřete stránku.

## <a name="define-location-profile"></a>Definování profilu skladového místa
1. Přejděte na **Navigační podokno > Moduly > Řízení skladu > Nastavení > Sklad > rofily umístění**. Definování profilů skladových míst je velmi důležité. Zde lze spravovat kapacitu seskupených skladových míst a také zásady týkající se toho, jaké zásoby budou uloženy a jak jsou uloženy. Profily skladového místa lze použít jako možnosti filtrování k řízení různých procesů správy skladu. Je nutné vytvořit profil skladového místa uživatele, chcete-li povolit WMS.
2. Klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **ID profilu skladového místa**.
4. Zadejte hodnotu do pole **Název**.
5. V poli **Formát umístění** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
7. Klikněte na odkaz na vybraném řádku v seznamu.
8. V poli **Typ umíssění** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
9. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
10. Klikněte na odkaz na vybraném řádku v seznamu.
11. Zaškrtněte nebo zrušte zaškrtnutí políčka **Povolit smíšené stavy zásob**. Tuto možnost povolte, pokud chcete povolit hodnoty smíšeného stavu zásob ve skladových místech, které budou seskupeny podle tohoto profilu skladového místa. 
12. Zaškrtněte nebo zrušte zaškrtnutí políčka **Pravidla přepisu pro dny dávky**. Tuto možnost povolte, chcete-li přepsat pravidlo pro určení, o kolik dnů se data vypršení platnosti skladové dávky mohou lišit, aby bylo možné míchat dávky skladových zásob nesplňující požadavky tohoto pravidla.  
13. Zaškrtnětenebo zrušte zaškrtnutí políčka **Povolit cyklickou inventuru**. Tuto možnost povolte, pokud chcete povolit zpracování cyklické inventury ve všech skladových místech, které budou seskupeny podle tohoto profilu skladového místa. 
14. Rozbalte nebo sbalte oddíl **Rozměry**. Karta Dimenze umožňuje definovat parametry a metody pro povolení přesných výpočtů kapacity vytížení v rámci každého skladového místa.  
15. Zavřete stránku.

## <a name="enable-warehouse-management-parameters"></a>Povolení parametrů řízení skladu
1. Přejděte na **Navigační podokno > Moduly > Řízení skladu > Nastavení > Parametry řízení skladu**. Aby bylo možné zpracovat práci skladu, je nutné nastavit parametry pro profil skladového místa uživatele, typ fázování umístění a typ konečného skladového místa. Jakmile bude odchozí proces končit u typu konečného skladového místa, který definujete, související výstupní transakce budou aktualizovány na hodnotu „Vydáno“.
2. Rozbalte oddíl **Profily umístění**.
3. V poli **Umístění uživatele** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Klikněte na odkaz na vybraném řádku v seznamu.
5. Rozbalte oddíl **Typy umístění**.
6. V poli **Přechodné skladové místo** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
7. Klikněte na odkaz na vybraném řádku v seznamu.
8. V poli **Typ konečného skladového místa** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
9. Klikněte na odkaz na vybraném řádku v seznamu.
10. Zavřete stránku.

## <a name="define-warehouse-zone-groups"></a>Definování skupin zón skladu
1. Přejděte na **Navigační podokno > Moduly > Řízení skladu > Nastavení > Sklad > Skupiny zón skladu**. Zóny skladu lze použít jako filtry k řízení různých procesů správy skladu. Před definováním zóny je nutné vytvořit skupiny zón.   
2. Klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **ID skupiny zón**.
4. Zadejte hodnotu do pole **Název skupiny zón**.
5. Zavřete stránku.

## <a name="define-warehouse-zones"></a>Definování zón skladu
1. Přejděte na **Navigační podokno > Moduly > Řízení skladu > Nastavení > Sklad > Zóny**.
2. Klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **ID zóny**.
4. Zadejte hodnotu do pole **Název zóny**.
5. V poli **ID skupiny zón** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
7. Klikněte na odkaz na vybraném řádku v seznamu.
8. Zavřete stránku.

## <a name="create-locations-using-the-location-setup-wizard"></a>Vytvoření skladových míst pomocí průvodce nastavením skladového místa
1. Přejděte na **Navigační podokno > Moduly > Řízení skladu > Nastavení > Sklad > Průvodce nastavením skladového místa**.
2. V poli **Sklad** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
3. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
4. Klikněte na odkaz na vybraném řádku v seznamu.
5. V poli **ID zóny** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
7. Klikněte na odkaz na vybraném řádku v seznamu.
8. V poli **ID profilu skladového místa** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
9. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
10. Klikněte na odkaz na vybraném řádku v seznamu.
11. Označte v seznamu vybraný řádek.
12. Zadejte číslo do pole **Od čísla**. Pole Od čísla a Do čísla definují počet skladových míst, která budou vytvořena. Například pokud nastavíte číslo Od na hodnotu 1 a Do na hodnotu 3 pro všechny čtyři řádky formátu skladového místa, vytvoří se 81 skladových míst (3x3x3x3).   
13. Zadejte číslo do pole **Do čísla**.
14. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
15. Zadejte číslo do pole **Od čísla**.
16. Zadejte číslo do pole **Do čísla**.
17. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
18. Zadejte číslo do pole **Od čísla**.
19. Zadejte číslo do pole **Do čísla**.
20. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
21. Zadejte číslo do pole **Od čísla**.
22. Zadejte číslo do pole **Do čísla**.
23. Klikněte na položku Vytvořit.

## <a name="create-locations-manually"></a>Ruční vytvoření skladových míst
1. Přejděte do nabídky **Řízení skladu > Nastavení > Sklad > Umístění**. Lze snadno ručně vytvořit skladová místa ve skladu. Název skladového místa a ID profilu umístění jsou povinné hodnoty. 
2. Klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **Sklad**.
4. Zadejte hodnotu do pole **Umístění**. Všimněte si, že zde vytváříte nové skladové místo, proto je nutné zadat nový jedinečný název, ne vybírat existující název.
5. Zadejte hodnotu do pole **ID profilu skladového místa**.
6. Zavřete stránku.

## <a name="define-pack-size-categories"></a>Definování kategorií velikosti balení
1. Přejděte do nabídky **Řízení skladu > Nastavení > Sklad > Kategorie velikosti balení**. Kategorie velikosti balení lze použít k seskupování položek, které mají podobné fyzické rozměry balení. V tomto příkladu se použije kategorie velikosti balení k řízení kapacity při výdejních skladových místech v rámci konkrétní zóny skladu. Všimněte si, že ID kategorie velikosti balení musí být přiřazeno k entitě uvolněného produktu, aby bylo možné jej použít jako součást zpracování skladových limitů.  
2. Klepněte na možnost **Nový**.
3. V poli **ID kategorie velikosti balení** zadejte hodnotu.
4. V poli **Název kategorie velikosti balení** zadejte hodnotu.
5. Zavřete stránku.

## <a name="define-location-stocking-limits"></a>Definice limitů pro místo uskladnění
1. Přejděte do nabídky **Řízení skladu > Nastavení > Sklad > Limity pro místo uskladnění**. Limity pro místo uskladnění umožňují zajistit, aby nebyla vytvořena práce vyžadující umístění zásob na skladové místo, které nemá fyzickou kapacitu pro zásoby.  
2. Klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **Sklad**.
4. Zadejte hodnotu do pole **ID profilu skladového místa**.
5. V poli **ID kategorie velikosti balení** zadejte hodnotu.
6. Zadejte číslo do pole **Množství**.
7. Klikněte na možnost **Uložit**.
8. Zavřete stránku.

## <a name="define-fixed-picking-locations"></a>Definování pevných výdejních skladových míst
1. Přejděte do nabídky **Řízení skladu > Nastavení > Sklad > Pevná skladová místa**. Můžete definovat skladová místa k použití pro produkt nebo variantu produktu. Je možné vytvořit více pevných skladových míst pro stejný produkt v rámci stejného skladu.     
2. Klepněte na možnost **Nový**.
3. Zadejte hodnotu do pole **Číslo zboží**.
4. Zadejte hodnotu do pole **Sklad**.
5. V poli **Umístění** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
6. Klikněte na odkaz na vybraném řádku v seznamu.
7. Zavřete stránku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
