---
title: Nastavení oceňovacích modelů
description: Tento postup popisuje, jak vytvořit novou knihu dlouhodobého majetku a přidružit ji ke skupině dlouhodobého majetku.
author: moaamer
ms.date: 12/03/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 71d256b600956a4e525cde626c958713f6258f5a
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727054"
---
# <a name="set-up-value-models"></a>Nastavení oceňovacích modelů

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../../includes/preview-banner.md)]

Tento postup popisuje, jak vytvořit novou knihu dlouhodobého majetku a přidružit ji ke skupině dlouhodobého majetku.

## <a name="create-a-book"></a>Vytvoření knihy
1. Přejděte do části **Dlouhodobý majetek \> Nastavení \> Knihy**.
2. Zvolte **Nové**.
3. Zadejte hodnotu do pole **Kniha**.
4. V poli **Popis** zadejte hodnotu.
5. Nastavte možnost **Výpočet odpisu** na **Ano**.

    Pokud je možnost **Výpočet odpisu** je nastavena na **Ano**, v návrzích odpisů bude zahrnuta přidružená kniha majetku. Pokud je tato hodnota nastavena na **Ne**, kniha majetku nebude automaticky odepsána.

6. V poli **Profil odpisu** zadejte nebo vyberte hodnotu.

    * Pro alternativní odpisový plán se rovněž používá označení přepínací způsob odpisu. Návrh odpisu se přepne na tento profil při výpočtu částky odpisu v alternativním profilu, která je rovna nebo větší než hodnota výchozího odpisového profilu.
    * Plán mimořádných odpisů se používá pro dodatečný odpis majetku při neobvyklých okolností. Například to můžete použít k záznamu odpisů, které je výsledkem živelné pohromy.
    * Pokud vyberete možnost **Vytvořit úpravy odpisů s úpravami základu**, úpravy odpisů se vytvoří automaticky při aktualizaci hodnoty majetku. V opačném případě ovlivní aktualizovaná hodnota majetku pouze budoucí výpočty odpisů.

7. Nastavte možnost **Vytvořit úpravy odpisů s úpravami základu** vyberte **Ano**.

    * Ve výchozím nastavení se do hlavní knihy zaúčtují transakce knihy dlouhodobého majetku. Zaúčtování knihy do hlavní knihy nicméně můžete zakázat nastavením hodnoty v poli **Zaúčtovat do hlavní knihy** na hodnotu **Ne**. Knihy, které nejsou zaúčtovány do hlavní knihy, se obvykle používají pro účely vykazování daně. Tato možnost vám dává větší flexibilitu k odstranění historických transakcí pro knihu majetku, protože transakce nebyly potvrzeny do hlavní knihy.
    * Ve výchozím nastavení je pole **Účtovací vrstva** nastaveno na hodnotu **Aktuální vrstva**, pokud je kniha zaúčtována do hlavní knihy, a na hodnotu **Žádná**, pokud kniha není zaúčtována do hlavní knihy. Aktualizujte hodnotu pole **Účtovací vrstva**, pokud mají být transakce pro tuto knihu zaúčtovány do jiné vrstvy.

8. Vypočítejte kladný odpis.

    * Ve výchozím nastavení je volba **Vypočítat kladný odpis** nastavena na **Ne**. Toto nastavení udává, že odpisy budou připisovat vybranou knihu majetku. Kromě toho jsou obě možnosti **Povolit zůstatkovou účetní hodnotu vyšší než pořizovací cena** a **Povolit zápornou zůstatkovou účetní hodnotu** nastaveny na **Ne** a nastavení lze nezávisle měnit. 
    * Pro vypočítání kladného odpisu nastavte možnost **Vypočítat kladný odpis** na **Ano**. Toto nastavení udává, že odpisy budou odepisovat knihu dlouhodobého majetku. Když je možnost **Vypočítat kladný odpis** nastavena na **Ano**, možnosti **Povolit zůstatkovou účetní hodnotu vyšší než pořizovací cena** a **Povolit zápornou zůstatkovou účetní hodnotu** budou automaticky nastaveny na **Ano** a budou uzamčeny. Tato uzamčení pomáhájí zajistit, že kladné odpisy budou aplikovány pouze na dlouhodobý majetek, který byl pořízen se zápornou účetní hodnotou (přípis). 

10. V poli **Kalendář** zadejte nebo vyberte hodnotu.

    Odvozené knihy budou zaúčtovávat transakce do různých knih najednou. Vytvoříte transakce s primární knihou a při zaúčtovávání se přesná kopie transakce zaúčtuje do odvozené knihy. Neexistuje žádný přepočet s transakcemi odvozených knih, proto není vhodné použít je pro transakce odpisů.

## <a name="associate-the-book-with-a-fixed-asset-group"></a>Přiřazení knihy ke skupině dlouhodobého majetku

1. Vyberte **Skupiny dlouhodobého majetku**.
2. Zadejte nebo vyberte hodnotu v poli **Skupina dlouhodobého majetku**.
3. Zadejte číslo do pole **Doba životnosti**.

    * Období odpisu se vypočítají po vložení doby životnosti majetku.
    * Způsob odpisu je možné nastavit podle potřeby pro daňové účely.
    * U dlouhodobého majetku, který je přidružen k leasingům, hodnota v poli **Doba životnosti** bude přepsána nižší hodnotou doby trvání leasingu v knize majetku a očekávané doby použitelnosti majetku. Pokud je možnost **Převod vlastnictví** nastaveno na **Ano** u leasingové knihy, hodnota v poli **Doba životnosti** bude vždy očekávanou dobou použitelnosti aktiva.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
