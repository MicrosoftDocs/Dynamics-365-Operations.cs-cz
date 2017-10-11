--- 
title: "Nastavení knih"
description: "Tento postup popisuje, jak vytvořit novou knihu dlouhodobého majetku a přidružit ji ke skupině dlouhodobého majetku."
author: saraschi2
manager: AnnBe
ms.date: 10/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 668fea64810524e8ce0c3833d25656c026f2780a
ms.openlocfilehash: 7e57b26c17d3bf773a719f9725d5f47dce2af6f7
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2017

---
# <a name="set-up-books"></a>Nastavení knih

[!include[task guide banner](../../includes/task-guide-banner.md)]

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

