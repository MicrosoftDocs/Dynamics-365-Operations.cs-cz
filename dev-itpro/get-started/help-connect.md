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

Toto téma popisuje komponenty systému nápovědy pro Microsoft Dynamics 365 pro operace. Poskytuje přehled o tom, jak připojit tyto komponenty a souhrnné informace o tom, jak vytvořit vlastní nápovědu. 

<a name="help-architecture"></a>Architektura nápovědy
-----------------

Následující obrázek ukazuje části 365 Dynamics pomoci operací systému. Systém nápovědy v produktu přebírá články z 365 Dynamics webu operace na https://docs.microsoft.com, jakož i vodítka úlohy uloženy v modelování obchodního procesu v Lifecycle Services (LCS). 
**Poznámka:** funkce uvedené v diagramu s hvězdičkou (\*) jsou plánované, ale nejsou k dispozici. [![Help architecture](./media/help-architecture.png)](./media/help-architecture.png)

## <a name="connecting-the-help-system"></a>Připojení systému nápovědy
Použití **parametry systému** stránky, správci systému připojit kusy implementace systému nápovědy. [![Formulář Parametry systému nápovědy nastavení](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) na **parametry systému** stránky, postupujte takto:

1.  **Důležité:** při prvním otevření **pomoci** kartu, musíte se připojit k poskytování služeb. Ujistěte se, klepněte na odkaz doprostřed formuláře, čekání na připojení, zavřete dialogové okno a klepněte na tlačítko **OK** na **parametry systému** stránky. [![Připojit k LCS](./media/connect-to-lcs-crop-1024x365.png "připojit k LCS")](./media/connect-to-lcs-crop.png)
2.  Vyberte projekt služby Lifecycle Services pro připojení.
3.  Vyberte knihovny BPM (v rámci vybraného projektu), ze kterých chcete načíst záznamy úkolů.
4.  Nastavte pořadí zobrazení knihoven BPM. Tato možnost určuje pořadí, ve kterém se záznamy úkolů z knihoven zobrazí v podokně **Nápověda**.

Po provedení těchto kroků můžete otevřít podokno **Nápověda** a kliknout na kartu **Průvodci úkolem**. Nyní uvidíte průvodce úkolem vztahující ke stránce, kterou máte aktuálně otevřenou v aplikaci Dynamics 365 for Operations. Pokud nebyly nalezeny žádné průvodce úkolem, můžete zadat klíčová slova pro upřesnění hledání.

### <a name="showing-translated-task-guides"></a>Zobrazení přeložených průvodců úkoly

Vodítka přeložený úloh dodáno nejdříve v květnu 2016 APQC Unified knihovny a knihovny Začínáme. Aby bylo možné v aplikaci Dynamics 365 for Operations zobrazit lokalizovanou nápovědu v podobě průvodce úkolem, ujistěte se, že jste připojeni ke knihovně pro květen. Jazyk, ve kterém průvodce úkolu se zobrazí v je řízen pro každého uživatele jazykové nastavení v části **možnosti**&gt;**Předvolby**. **Poznámka:** I když mnoho průvodců úkolem již bylo přeloženy, klient Dynamics 365 for Operations aktuálně nezobrazuje názvy přeložených průvodců úkolem. Také jsou k dispozici v překladu v knihovně může pouze úkol vodítka, vydané v únoru 2016. Aktualizovanou knihovnou s další překlady zpřístupníme později.

-   Pokud průvodce úkolem byl přeložen, veškerý text průvodce úkolem se při otevření daného průvodce zobrazí ve vybraném jazyce.
-   Pokud průvodce úkolem zatím nebyl přeložen, při otevření daného průvodce se zobrazí ve vybraném jazyce pouze některý text (text ovládacích prvků).

## <a name="creating-custom-help"></a>Vytváření vlastních nápověd
Vlastní nápovědu pro implementaci aplikace Dynamics 365 for Operations můžete vytvořit vytvořením záznamů úkolu, které odpovídají vaší implementaci, a jejich uložením do knihovny obchodního procesu LCS. Pro partnery platí, že pokud knihovnu nastavíte jako podnikovou knihovnu a zahrnete ji do řešení, bude k dispozici vašim odběratelům. Můžete vytvořit také kopii sjednocené globální knihovny APQC a poté otevřít kopii z ní otevřít záznamy úloh, upravit je a uložit záznamy s provedenými změnami. Další informace naleznete v tématu [jak vytvořit úlohy nahrávání použít jako dokumentaci nebo školení](../user-interface/task-recorder.md).

<a name="see-also"></a>Viz také
--------

[Help overview](help-overview.md)

[Přehled Záznamník úkolů](../user-interface/task-recorder.md)

[Postup vytvoření záznamu úloh pro použití jako dokumentace nebo školení](../user-interface/task-recorder-training-docs.md)

[Vytvoření nové knihovny školení pro Dynamics 365 pro operace v rámci poskytování služeb pomocí Záznamníku úkolů (externí odkaz)](https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax)


