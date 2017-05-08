---
title: "Připojení k systému nápovědy"
description: "Toto téma popisuje součásti systému nápovědy aplikace Microsoft Dynamics 365 for Operations a poskytuje přehled o způsobu jejich propojení a shrnutí postupu pro vytvoření vlastní nápovědy."
author: margoc
manager: AnnBe
ms.date: 2015-12-03 22 - 12 - 49
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SystemParameters
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16141
ms.assetid: 0b9c8630-9474-4473-80fd-7db5d54b2275
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 5ac5e30cff2239f601778001368fa7aaba478f5c
ms.lasthandoff: 03/31/2017


---

# <a name="connect-the-help-system"></a>Připojení k systému nápovědy

Toto téma popisuje komponenty systému nápovědy aplikace Dynamics 365 for Operations. Poskytuje přehled o tom, jak připojit tyto komponenty, a souhrnné informace o tom, jak vytvořit vlastní nápovědu. 

<a name="help-architecture"></a>Architektura nápovědy
-----------------

Následující obrázek znázorňuje části systému nápovědy aplikace Microsoft Dynamics 365 for Operations. Systém nápovědy v produktu přebírá články z webu https://docs.microsoft.com nápovědy k aplikaci Dynamics 365 for Operations, jakož i průvodce úkolem uložené v modulu k modelování podnikových procesů v aplikaci Microsoft Dynamics Lifecycle Services (LCS). 
**Poznámka:** Funkce uvedené v diagramu s hvězdičkou (\*) jsou plánované, ale nejsou ještě k dispozici. [![Architektura nápovědy](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Připojení systému nápovědy
Pomocí stránky **Systémové parametry** správci systému připojí části systému nápovědy pro implementaci. [![Formulář Nastavení nápovědy k systémovým parametrům](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) Na stránce **Systémové parametry** proveďte následující kroky:

1.  **Upozornění:** při prvním otevření karty **Nápověda** je nutné se připojit ke Lifecycle Services. Nezapomeňte klepnout na odkaz v polovině formuláře, počkat na připojení, zavřít dialogové okno a klepnout na tlačítko **OK** k získání stránky **Parametry systému**.[![Připojit k LCS](./media/connect-to-lcs-crop-1024x365.png "Připojit k LCS")](./media/connect-to-lcs-crop.png)
2.  Vyberte projekt služby Lifecycle Services pro připojení.
3.  Vyberte knihovny BPM (v rámci vybraného projektu), ze kterých chcete načíst záznamy úkolů.
4.  Nastavte pořadí zobrazení knihoven BPM. Tato možnost určuje pořadí, ve kterém se záznamy úkolů z knihoven zobrazí v podokně **Nápověda**.

Po provedení těchto kroků můžete otevřít podokno **Nápověda** a kliknout na kartu **Průvodci úkolem**. Nyní uvidíte průvodce úkolem vztahující ke stránce, kterou máte aktuálně otevřenou v aplikaci Dynamics 365 for Operations. Pokud nebyly nalezeny žádné průvodce úkolem, můžete zadat klíčová slova pro upřesnění hledání.

### <a name="showing-translated-task-guides"></a>Zobrazení přeložených průvodců úkoly

Přeložení průvodci úkolem byli poprvé vydání v knihovně APQC Unified Library pro květen 2016 a v knihovně Začínáme. Aby bylo možné v aplikaci Dynamics 365 for Operations zobrazit lokalizovanou nápovědu v podobě průvodce úkolem, ujistěte se, že jste připojeni ke knihovně pro květen. Jazyk, ve kterém se průvodce úkolem zobrazí, je řízen pro každého uživatele v jazykovém nastavení v části **Možnosti** &gt; **Předvolby**. **Poznámka:** I když mnoho průvodců úkolem již bylo přeloženy, klient Dynamics 365 for Operations aktuálně nezobrazuje názvy přeložených průvodců úkolem. Stejně tak pouze průvodci úkolem vydaní v únoru jsou momentálně k dispozici v překladu v knihovně pro únor 2016. Aktualizovanou knihovnou s další překlady zpřístupníme později.

-   Pokud průvodce úkolem byl přeložen, veškerý text průvodce úkolem se při otevření daného průvodce zobrazí ve vybraném jazyce.
-   Pokud průvodce úkolem zatím nebyl přeložen, při otevření daného průvodce se zobrazí ve vybraném jazyce pouze některý text (text ovládacích prvků).

## <a name="creating-custom-help"></a>Vytváření vlastních nápověd
Vlastní nápovědu pro implementaci aplikace Dynamics 365 for Operations můžete vytvořit vytvořením záznamů úkolu, které odpovídají vaší implementaci, a jejich uložením do knihovny obchodního procesu LCS. Pro partnery platí, že pokud knihovnu nastavíte jako podnikovou knihovnu a zahrnete ji do řešení, bude k dispozici vašim odběratelům. Můžete vytvořit také kopii sjednocené globální knihovny APQC a poté otevřít kopii z ní otevřít záznamy úloh, upravit je a uložit záznamy s provedenými změnami. Další informace naleznete v tématu [Vytvoření záznamu úkolu jako dokumentace nebo školení](../user-interface/task-recorder.md).

<a name="see-also"></a>Viz také
--------

[Přehled nápovědy](help-overview.md)

[Přehled záznamníku úloh](../user-interface/task-recorder.md)

[Postup vytvoření záznamu úloh pro použití jako dokumentace nebo školení](../user-interface/task-recorder-training-docs.md)

[Vytvoření nových knihoven pro školení pro aplikaci Dynamics 365 for Operations v rámci služby Lifecycle Services pomocí Záznamníku úloh (externí odkaz)](https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax)

