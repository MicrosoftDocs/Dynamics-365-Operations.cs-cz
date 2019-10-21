---
title: Nastavení oceňovacích modelů
description: Tento postup popisuje, jak vytvořit novou knihu dlouhodobého majetku a přidružit ji ke skupině dlouhodobého majetku.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a528bd12552d5ce100027c9a789f6e1bdc597b66
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186847"
---
# <a name="set-up-value-models"></a>Nastavení oceňovacích modelů

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje, jak vytvořit novou knihu dlouhodobého majetku a přidružit ji ke skupině dlouhodobého majetku. Využívá účetní role a ukázková data pro právnické osoby USMF.


## <a name="create-a-book"></a>Vytvoření knihy
1. Přejděte do části Dlouhodobý majetek > Nastavení > Knihy.
2. Klikněte na položku Nová.
3. Zadejte hodnotu do pole Kniha.
4. Zadejte nějakou hodnotu do pole Popis.
    * Pokud je vybrána možnost Výpočet odpisu, přidružené knihy majetku budou zahrnuty v návrzích odpisů. Pokud není hodnota vybrána, nebude se kniha majetku automaticky odepisovat.  
5. Vyberte možnost Ano v poli Výpočet odpisu.
6. V poli Profil odpisu zadejte nebo vyberte hodnotu.
    * Pro alternativní odpisový plán se rovněž používá označení přepínací způsob odpisu. Návrh odpisu se přepne na tento profil při výpočtu částky odpisu v alternativním profilu, která je rovna nebo větší než hodnota výchozího odpisového profilu.  
    * Plán mimořádných odpisů se používá pro dodatečný odpis majetku při neobvyklých okolností. Například to můžete použít k záznamu odpisů, které je výsledkem živelné pohromy.  
    * Pokud vyberete možnost Vytvořit úpravy odpisů s úpravami základu, úpravy odpisů se vytvoří automaticky při aktualizaci hodnoty majetku. Jestliže není možnost zaškrtnuta, aktualizované hodnoty majetku ovlivní pouze výpočty odpisů do budoucna.  
7. V poli Vytvořit úpravy odpisů s úpravami základu vyberte Ano.
    * Ve výchozím nastavení se do hlavní knihy zaúčtují transakce knihy dlouhodobého majetku. Zaúčtování knihy do hlavní knihy můžete zakázat nastavením hodnoty v poli Zaúčtovat do hlavní knihy na hodnotu Ne. Knihy, které nebudou zaúčtovány do hlavní knihy, se obvykle používají pro účely vykazování daně. To vám dává další flexibilitu k odstranění historických transakcí pro knihu majetku, protože nebyly potvrzeny do hlavní knihy.  
    * Pokud se kniha zaúčtuje do hlavní knihy, účtovací vrstva bude mít ve výchozím nastavení hodnotu Aktuální vrstva a pokud se do hlavní knihy nezaúčtuje, bude mít hodnotu Žádný. Aktualizujte Účtovací vrstvu, pokud potřebujete, aby transakce pro tuto knihu byly zaúčtovány do jiné vrstvy.  
8. V poli Kalendář zadejte nebo vyberte hodnotu.
    * Odvozené knihy budou zaúčtovávat transakce do různých knih najednou. Vytvoříte transakce s primární knihou a při zaúčtovávání se přesná kopie transakce zaúčtuje do odvozené knihy. Neexistuje žádný přepočet s transakcemi odvozených knih, proto není vhodné použít je pro transakce odpisů.  

## <a name="associate-the-book-with-a-fixed-asset-group"></a>Přiřazení knihy ke skupině dlouhodobého majetku
1. Klikněte na Skupiny dlouhodobého majetku.
2. Zadejte nebo vyberte hodnotu v poli Skupina dlouhodobého majetku.
3. Zadejte číslo do pole Doba životnosti.
    * Všimněte si, že hodnota pole Období odpisu se vypočítá po nastavení doby životnosti.  
    * Způsob odpisu je možné nastavit podle potřeby pro daňové účely.  

