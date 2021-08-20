---
title: Vytvoření modelu konfigurace produktu
description: Tento postup popisuje způsob vytvoření modelu konfigurace produktu a zadání základních informací, jako například atributy a dílčí komponenty.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0ff03c13e1d9b7a15a0237b8248c734aa879166d2db2cebeb4a98db699e3de95
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748732"
---
# <a name="create-a-product-configuration-model"></a>Vytvoření modelu konfigurace produktu

[!include [banner](../../includes/banner.md)]

Tento postup popisuje způsob vytvoření modelu konfigurace produktu a zadání základních informací, jako například atributy a dílčí komponenty. K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.


## <a name="create-a-product-model"></a>Vytvoření modelu výrobku

1. Přejděte na **Řízení informací o produktech \> Produkty \> Modely konfigurace produktu**.
1. Zvolte **Nové**.
1. Zadejte hodnotu do pole **Název**.
1. Zadejte hodnotu do pole **Popis**.
1. Vyberte volbu v poli **Strategie řešitele**.
    * Strategie řešitele určuje způsob zpracování omezení v modelu konfigurace produktu založeného na omezeních. Tento výběr může mít vliv na výkon modelu konfigurace produktu.  
1. Zadejte hodnotu do pole **Název**.
    * Kořenová komponenta představuje model konfigurace produktu, ale lze ji použít také v jiných modelech výrobků.  
1. Vyberte **OK**.
1. V poli **Znovu použít konfigurace** vyberte možnost.
    * Je-li parametr opakovaného použití konfigurace nastaven na hodnotu Ano, systém zkontroluje v každé konfigurační relaci, zda byla nalezena identická konfigurace, a pokud byla nalezena přesná shoda, použije ji znovu.  

## <a name="add-attributes"></a>Přidat atributy

1. Rozbalte sekci **Atributy**.
2. Vyberte **přidat**.
3. Označte na seznamu vybraný řádek.
4. Zadejte hodnotu do pole **Název**.
5. Do pole **Název řešitele** zadejte hodnotu.
    * Název řešitele je používán řešitelem omezení konfigurátoru výrobku. Nesmí obsahovat mezery ani speciální znaky kromě _ (podtržítko).  
6. Zadejte hodnotu do pole **Popis**.
    * Text popis se zobrazí uživateli konfigurace, a může proto sloužit jako pomoc při výběru správné hodnoty atributu.  
7. V poli **Typ atributu** zadejte nebo vyberte hodnotu.
    * Typ atributu určuje, které hodnoty jsou pro atribut k dispozici.  
8. Zaškrtněte políčko položky **Zahrnout do opakovaného použití**.
    * Tato možnost je k dispozici pouze v případě, že je vybrána možnost Znovu použít konfigurace. Zaškrtávací políčko Zahrnutí atributu do opětovného použití znamená, že tento atribut bude zvážen, když bude systém hledat přesnou shodu.  

## <a name="add-subcomponents"></a>Přidat dílčí komponenty

1. Rozbalte sekci **Dílčí komponenty**.
2. Vyberte **přidat**.
3. Označte na seznamu vybraný řádek.
4. Zadejte hodnotu do pole **Název**.
5. Do pole **Název řešitele** zadejte hodnotu.
6. Zadejte hodnotu do pole **Popis**.
7. V poli **Komponenty** zadejte nebo vyberte hodnotu.
    * Každý dílčí komponent musí odkazovat na definici komponenty. Tento návrh podporuje opakované použití komponent a zajišťuje, že po definování komponenty ji je možné použít v mnoha modelech výrobků.  
8. Zvolte **Uložit**.
9. Vyberte **Podrobnosti řádku kusovníku**.
    * Formulář Podrobnosti řádku Kusovníku umožňuje uživatelům vybrat požadované vlastnosti pro dílčí komponentu. Všechny vlastnosti mohou mít stanovenou pevnou hodnotu nebo namapovanou hodnotu k atributu. Mapování na atribut má za výsledek, že vlastnosti řádku kusovníku získají odlišné hodnoty v závislosti na výběru konfigurace.  
10. V poli **Číslo položky** zadejte nebo vyberte hodnotu.
    * Každý dílčí představuje základní konfigurovatelný produkt s technologií konfigurace založenou na omezeních. Odkaz je vytvořen prostřednictvím čísla položky.  
11. Zaškrtněte políčko položky **Nastavit**.
12. Vyberte možnost **Ano** v poli **Výpočet**.
    * Možnost nastavení výpočtu zajišťuje, že výrobek bude zahrnut při spuštění výpočtu nákladů pro produkt.  
13. Vyberte kartu **Nastavení**.
14. Zaškrtněte políčko položky **Nastavit**.
15. Zadejte číslo do pole **Množství**.
    * Pole množství určuje, kolik tohoto produktu bude spotřebováno v konfigurovaném produktu.  
16. Zaškrtněte políčko položky **Nastavit**.
17. V poli **Podle sérií** zadejte číslo.
18. Vyberte **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]