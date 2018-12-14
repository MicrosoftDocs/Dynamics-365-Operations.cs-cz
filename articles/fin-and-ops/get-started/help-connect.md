---
title: "Připojení k systému nápovědy"
description: "Toto téma popisuje součásti systému nápovědy aplikace Microsoft Dynamics 365 for Finance and Operations a obsahuje přehled způsobu jejich propojení a shrnutí postupu vytvoření vlastní nápovědy."
author: margoc
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 87ca6afe817d27de12479f1b7d8155d11d800233
ms.openlocfilehash: a2ca5f5302751ad2c4ddc3c6921a8a9b6c2d57df
ms.contentlocale: cs-cz
ms.lasthandoff: 12/04/2018

---

# <a name="connect-the-help-system"></a>Připojení k systému nápovědy

[!include [banner](../includes/banner.md)]

Toto téma popisuje součásti systému nápovědy aplikace Microsoft Dynamics 365 for Finance and Operations. Poskytuje přehled o tom, jak připojit tyto komponenty, a souhrnné informace o tom, jak vytvořit vlastní nápovědu. 

## <a name="help-architecture"></a>Architektura nápovědy
Následující obrázek znázorňuje části systému nápovědy aplikace Finance and Operations. Systém nápovědy v produktu přebírá články z webu aplikace Finance and Operations na adrese https://docs.microsoft.com a také z průvodců záznamem úloh uložených v modulu modelování podnikových procesů ve službě Lifecycle Services (LCS). 
> [!NOTE]
> Funkce označené v diagramu hvězdičkou (\*) jsou plánované, ale nejsou zatím k dispozici. [![Architektura nápovědy](./media/help-architecture.png)](./media/help-architecture.png)


## <a name="connecting-the-help-system"></a>Připojení systému nápovědy
> [!NOTE]
> Karta **Průvodci záznamem úloh** není v současnosti v aplikacích Microsoft Dynamics 365 for Talent a Microsoft Dynamics 365 for Retail k dispozici. Funkci zpřístupníme v budoucí verzi. Průvodci v prostředí Začínáme v aplikaci Talent jsou i nadále k dispozici a zabývají se základními funkcemi. Na webu docs.microsoft.com ([docs.microsoft.com/dynamics365/unified-operations](../../index.md)) jsou také k dispozici pokyny pro aplikaci Retail i Talent.


Pomocí stránky **Systémové parametry** správci systému připojí části systému nápovědy pro implementaci. [![Formulář Nastavení nápovědy k systémovým parametrům](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) Na stránce **Systémové parametry** proveďte následující kroky:

> [!IMPORTANT]
> Při prvním otevření karty **Nápověda** je nutné se připojit k službě Lifecycle Services. Nezapomeňte klepnout na odkaz v polovině formuláře, počkat na připojení, zavřít dialogové okno a klepnout na tlačítko **OK** k získání stránky **Parametry systému**.[![Připojit k LCS](./media/connect-to-lcs-crop-1024x365.png "Připojit k LCS")](./media/connect-to-lcs-crop.png)

1.  Vyberte projekt služby Lifecycle Services pro připojení.
2.  Vyberte knihovny BPM (v rámci vybraného projektu), ze kterých chcete načíst záznamy úkolů.
    - U aplikace Finance and Operations vyberte pro obsah společnosti Microsoft nejnovější APQC Unified Library for Finance and Operations. 
    - Pro modul Retail vydáme knihovnu v blízké době. 
    - Pro aplikaci Talent není třeba knihovnu vybírat – připojení ke správné knihovně se nastaví automaticky. 

3.  Nastavte pořadí zobrazení knihoven BPM. Tato možnost určuje pořadí, ve kterém se záznamy úkolů z knihoven zobrazí v podokně **Nápověda**.

Po dokončení těchto kroků můžete otevřít podokno **Nápověda** a kliknutí na kartu **Průvodci záznamem úloh**. Zobrazí se vám nyní průvodci záznamem úloh, které se vztahují ke stránce, na které se momentálně v aplikaci Finance and Operations nacházíte. Pokud nebyly nalezeny žádné průvodce úkolem, můžete zadat klíčová slova pro upřesnění hledání.

### <a name="showing-translated-task-guides"></a>Zobrazení přeložených průvodců úkoly

Přeložení průvodci úkolem byli poprvé vydání v knihovně APQC Unified Library pro květen 2016 a v knihovně Začínáme. Chcete-li v aplikaci Finance and Operations zobrazit lokalizovanou nápovědu k průvodci záznamem úloh, zkontrolujte, zda máte připojenou knihovnu z května. Jazyk, ve kterém se průvodce úkolem zobrazí, je řízen pro každého uživatele v jazykovém nastavení v části **Možnosti** &gt; **Předvolby**. 

> [!NOTE]
> I když mnoho průvodců záznamem úloh již bylo přeloženo, klient aplikace Finance and Operations v současnosti nezobrazuje jejich přeložené názvy. Stejně tak pouze průvodci úkolem vydaní v únoru jsou momentálně k dispozici v překladu v knihovně pro únor 2016. Aktualizovanou knihovnou s další překlady zpřístupníme později.
> -   Pokud průvodce úkolem byl přeložen, veškerý text průvodce úkolem se při otevření daného průvodce zobrazí ve vybraném jazyce.
> -   Pokud průvodce úkolem zatím nebyl přeložen, při otevření daného průvodce se zobrazí ve vybraném jazyce pouze některý text (text ovládacích prvků).

## <a name="creating-custom-help"></a>Vytváření vlastních nápověd
Můžete použít průvodce záznamem úloh k vytvoření vlastní nápovědy, nebo připojit své webové stránky k panelu Nápověda. 

### <a name="create-custom-help-with-task-guides"></a>Vytvoření vlastní nápovědy pomocí průvodců záznamem úloh
Vlastní nápovědu pro aplikace Finance and Operations a Retail můžete vytvořit tak, že vytvoříte záznamy úloh, které odpovídají vaší implementaci, a uložíte je do knihovny obchodního procesu LCS. Pro aplikaci Talent nelze vlastní průvodce záznamem úloh vytvořit. 

Pro partnery platí, že pokud knihovnu nastavíte jako podnikovou knihovnu a zahrnete ji do řešení, bude k dispozici vašim odběratelům. Můžete vytvořit také kopii sjednocené globální knihovny APQC a poté otevřít kopii z ní otevřít záznamy úloh, upravit je a uložit záznamy s provedenými změnami. Další informace naleznete v tématu [Vytvoření záznamu úkolu jako dokumentace nebo školení](../../dev-itpro/user-interface/task-recorder.md).

### <a name="connect-a-custom-site"></a>Připojení vlastního webu
Společnost Microsoft poskytla dokument white paper a vzorový kód, které popisují způsob vytvoření a připojení vlastního webu nápovědy k panelu Nápověda. Další informace naleznete zde: 
- [Vytvoření vlastní nápovědy pro Finance and Operations (dokument white paper)](https://go.microsoft.com/fwlink/?linkid=2041185)
- [Úložiště GitHub vlastní nápovědy](https://github.com/microsoft/dynamics356f-o-custom-help)



<a name="additional-resources"></a>Další zdroje
--------

[Přehled nápovědy](help-overview.md)

[Přehled záznamníku úloh](../../dev-itpro/user-interface/task-recorder.md)

[Postup vytvoření záznamu úloh pro použití jako dokumentace nebo školení](../../dev-itpro/user-interface/task-recorder-training-docs.md)





