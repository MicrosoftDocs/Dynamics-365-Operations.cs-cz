---
title: "Přehled nápovědy"
description: "V tomto článku je přehled součástí systému nápovědy aplikace Microsoft Dynamics 365 for Operations. Také je zde vysvětleno, jak můžete poskytnout vlastní dokumentaci a školení pro vaši organizaci."
author: margoc
manager: AnnBe
ms.date: 2015-12-04 02 - 12 - 46
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 16381
ms.assetid: 018c148c-9cbd-41e0-8186-d75dbf66288f
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 240060606c8a2955c3f0a0d47fb25b0cde64c187
ms.lasthandoff: 03/31/2017


---

# <a name="help-overview"></a>Přehled nápovědy

V tomto článku je přehled součástí systému nápovědy aplikace Microsoft Dynamics 365 for Operations. Také je zde vysvětleno, jak můžete poskytnout vlastní dokumentaci a školení pro vaši organizaci. 

Microsoft Dynamics 365 for Operations zahrnuje zcela nový systém nápovědy, který je založen na dvou hlavních součástech:

-   Web s dokumentací
-   Průvodci úkoly

Wiki články i průvodce úkoly lze použít z podokna Nápověda aplikace Dynamics 365 for Operations, jak je uvedeno na následujícím snímku obrazovky. [![Podokno nápověda](./media/help-pane-ops-task-guides-1024x741.png)](./media/help-pane-ops-task-guides.png) Tento článek popisuje systém nápovědy a vysvětluje, jak lze vytvořit vlastní dokumentaci a zdroje školení pro vaši organizaci.

## <a name="help-on-docsmicrosoftcom"></a>Nápověda na webu docs.microsoft.com
Primární zdroj dokumentace produktu pro Dynamics 365 for Operations je web docs.microsoft.com site ([docs.microsoft.com/dynamics365/operations](https://docs.microsoft.com/en-us/dynamics365/#pivot=solutions&panel=solutions_operations). Web nabízí následující možnosti:

-   **Přístup k nejaktuálnějšímu obsahu** – web nám poskytuje rychlejší a pružnější způsob vytváření, provedení a aktualizaci dokumentace k produktům. Díky tomu pomáhá zajistit, že budete mít přístup k aktuálním technickým informacím.
-    **Obsah vytvořený odborníky** – web poskytuje lepší sadu dokumentace k produktu, kterou mohou vylepšovat členové komunity uvnitř i mimo aplikaci Microsoft.
-   ** Přístup k různým typům obsahu** – web umožňuje rychlý přístup k různým typům obsahu o aplikaci Dynamics 365 for Operations, například prezentacím Microsoft Office Mix, průvodcům úkoly, videím a wiki článkům.
-    **Obsah, který podporuje obchodní procesy** – web zahrnuje obsah založený na obchodní procesy, který využívá modul k modelování obchodních procesů (BPM) ve službě Microsoft Dynamics Lifecycle Services (LCS).

Přenesli jsme veškerý obsah z naší předchozí nápovědy wiki do dokumentů. Z našeho nového webu jsme nadšení a doufáme, že budete také.

### <a name="when-can-we-use-it"></a>Jak ji můžeme používat?

Na wiki si můžete číst obsah dokumentů – je zcela veřejný a prohledávatelný a nevyžaduje přihlášení. K hledání obsahu můžete použít kterýkoli svůj oblíbený vyhledávač. Články na webu můžete komentovat, pokud chcete, po přihlášení účtu GitHub.


## <a name="task-guides"></a>Průvodci úkoly
Průvodce záznamem úloh je kontrolovaný, řízený a interaktivní způsob, který vás provede kroky daného úkolu nebo obchodního procesu. Je možné otevřít (přehrát) Průvodce záznamem úloh v podokně Nápověda. Po prvním kliknutí na Průvodce záznamem úloh se v podokně Nápověda zobrazí podrobné pokyny pro úkol. Nově jsou k dispozici lokalizovaní průvodci záznamem úloh. [![Zobrazení čtení Průvodce záznamem úloh](./media/task-guide-ops-1024x742.png)](./media/task-guide-ops.png) Chcete-li zažít řízenou interaktivní zkušenost, klikněte na možnost **Spustit průvodce záznamem úloh** v dolní části podokna Nápověda. Černá ukazatel otevře a určuje akci, kterou je třeba provést. Postupujte podle pokynů v uživatelském rozhraní a zadejte data podle pokynů. [![Pokyn ke kroku průvodc záznamem úloh](./media/task-guide-step-1-ops.png)](./media/task-guide-step-1-ops.png) **Důležité:** Data, která zadáte při přehrávání průvodce úkolem, jsou pravdivá. Pokud jste ve výrobním prostředí, budou zadána data, která skutečně používáte.

### <a name="it-all-begins-with-task-recorder"></a>Vše začíná v Záznamníku úkolů

Průvodci úkolem se vytvoří pomocí Záznamníku úkolů. Při použití Záznamníku úkolů jsou zaznamenány všechny akce, které provedete v uživatelském rozhraní aplikace Dynamics 365 for Operations (například kliknutí na nabídky, změna nastavení a zadávání dat). Kroky, které zaznamenáte, jsou souhrnně označovány termínem záznam úkolu. Jak jsme vysvětlili v předchozím oddílu, lze zobrazit záznamy úloh v podokně Nápověda a přehrát jako průvodce úkolem. Existují však další možnosti, jak lze použít záznamy úloh:

-   **Uložení záznamu úkolu do BPM** – Lze uložit záznam úkolu na řádek v hierarchii knihovny BPM ve službě LCS. Při uložení záznamu úkol do BPM bude vygenerován vývojový diagram společně s kroky záznamu. **Poznámka:** Chcete-li zobrazit záznam úkolu v podokně Nápověda aplikace Dynamics 365 for Operations a přehrát jej jako průvodce úkolem, musíte záznam uložit do knihovny BPM.
-   **Uložení záznamů úkolů jako jako dokumentů Word** – Uložením záznamu úkolu jako dokumentu aplikace Microsoft Word můžete snadno vytvářet tisknutelné přepisy školení pro vaši organizaci.

Další informace o průvodci záznamem úloh viz [Záznamník úloh v Dynamics 365 for Operations](../user-interface/task-recorder.md).

### <a name="creating-customized-task-recordings"></a>Vytvoření přizpůsobených záznamů úkolů

Můžete vytvořit vlastní záznamy úkolů nebo můžete stáhnout a upravit záznam úkolu, který poskytuje společnost Microsoft. Proto můžete vytvořit upravenou nápovědu pro vaši organizaci, které odpovídá konkrétní implementaci aplikace Dynamics 365 for Operations. Chcete-li zobrazit záznam úloh v podokně Nápověda aplikace Dynamics 365 for Operations a přehrát jej jako průvodce záznamem úloh, musíte záznam uložit do knihovny BPM v LCS. Pro partnery platí, že pokud knihovnu nastavíte jako podnikovou knihovnu a zahrnete ji do řešení, bude k dispozici vašim odběratelům. Úplné pokyny viz [Vytváření dokumentace nebo školení pomocí záznamu úloh](../user-interface/task-recorder.md).

## <a name="in-product-help"></a>Nápověda v produktu
Chcete-li získat přístup k obsahu nápovědy v aplikaci Dynamics 365 for Operations, klikněte na ikonu **Nápověda** (**?**) a vyberte Nápovědna nebo stiskněte klávesy Ctrl + Shift +?. V obou případech se otevře podokno Nápověda. Z podokna Nápověda můžete otevřít články nebo průvodce záznamem úloh. [![](./media/help-pane-wiki-1024x684.png)](./media/help-pane-wiki.png)

### <a name="accessing-articles-from-the-help-pane"></a>Přístup k článkům z podokna Nápověda

Z podokna Nápověda můžete otevřít články, které se týkají klienta aplikace Dynamics 365 for Operations. Při prvním otevření podokna nápovědy a kliknutí na kartu **Wiki** uvidíte články, které se vztahují ke stránce, kterou máte aktuálně otevřenou v aplikaci Dynamics 365 for Operations. Pokud nebyly nalezeny žádné články, můžete zadat klíčová slova pro upřesnění hledání. Po kliknutí na článek v podokně Nápověda se nová záložka otevře v prohlížeči a zobrazí se wiki článek. 

### <a name="accessing-task-guides-from-the-help-pane"></a>Přístup k průvodcům záznamem úloh z podokna Nápověda

Před zobrazením průvodců záznamem úloh v podokně **Nápověda** musí správce systému přejít na stránku Systémové parametry v aplikaci Dynamics 365 for Operations a konfigurovat některá nastavení. **Poznámky:**

-   Než bude možné konfigurovat nápovědu, musíte být přihlášeni pomocí účtu ve stejném klientovi, jako ve kterém je aplikace Dynamics 365 for Operations nasazena.
-   Není možné připojit se do knihovny LCS z instance aplikace Dynamics 365 for Operations spuštěné na místním virtuálním pevném disku (VHD).

[![Formulář Nastavení nápovědy k systémovým parametrům](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) Na stránce **Systémové parametry** proveďte následující kroky:

1.  **Upozornění: **při prvním otevření karty Nápověda je nutné se připojit ke Lifecycle Services. Nezapomeňte klepnout na odkaz v polovině formuláře, počkat na připojení, zavřít dialogové okno a klepnout na tlačítko OK pro přístup k formuláři parametrů..[![Připojit k LCS](./media/connect-to-lcs-crop-1024x365.png)](./media/connect-to-lcs-crop.png)
2.  Vyberte projekt služby Lifecycle Services pro připojení.
3.  Vyberte knihovny BPM (v rámci vybraného projektu), ze kterých chcete načíst záznamy úkolů.
4.  Nastavte pořadí zobrazení knihoven BPM. Tato možnost určuje pořadí, ve kterém se záznamy úkolů z knihoven zobrazí v podokně Nápověda.

Jakmile správce systému provede tyto kroky, můžete otevřít podokno Nápověda a kliknout na kartu **Průvodci úkolem**. Nyní uvidíte průvodce záznamem úloh vztahující ke stránce, kterou máte aktuálně otevřenou v aplikaci Dynamics 365 for Operations. Pokud nebyli nalezeni žádní průvodci záznamem úloh, můžete zadat klíčová slova pro upřesnění hledání. Po kliknutí na Průvodce záznamem úloh v podokně Nápověda se v podokně Nápověda zobrazí podrobné pokyny a můžete také přehrát průvodce úkolem. [![Zobrazení Průvodce záznamem úloh pro čtení](./media/task-guide-ops-1024x742.png)](./media/task-guide-ops.png)

### <a name="where-are-the-translated-task-guides"></a>Kde jsou přeloženi průvodci záznamem úloh?

Přeložení průvodci záznamem úloh jsou v knihovnách "Všechny jazyky" v názvu. Aby bylo možné v aplikaci Dynamics 365 for Operations zobrazit lokalizovanou nápovědu v podobě průvodce záznamem úloh, musíte být připojení k vhodné knihovně. Jazyk, ve kterém se průvodce záznamem úloh zobrazí, je řízen pro každého uživatele v jazykovém nastavení v části **Možnosti** &gt; **Předvolby**. 
-   Pokud byl průvodce záznamem úloh přeložen, veškerý text Průvodce záznamem úloh se při otevření daného průvodce zobrazí ve vybraném jazyce.
-   Pokud Průvodce záznamem úloh zatím nebyl přeložen, při otevření daného průvodce se zobrazí ve vybraném jazyce pouze některý text (text ovládacích prvků).

## <a name="additional-resources"></a>Další prostředky
V následující tabulce jsou uvedeny weby, které poskytují obsah aplikace Dynamics 365 for Operations. Naše weby s obsahem jsou uspořádány pro podporu cyklu odběratele. Každá fáze je podporována jinou sadou webu. Weby s hvězdičkou (\*) u názvu vyžadují přihlášení pomocí účtu, který je přidružen k plánu služby.

| Pracoviště                                                                     | popis                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Docs.microsoft.com](https://docs.microsoft.com/en-us/dynamics365/#pivot=solutions&panel=solutions_operations) | Hostitelé nebo odkazy na veškerou dokumentaci k produktům pro aplikaci Dynamics 365 for Operations.                                                                                                                                                               |
| [Lifecycle Services](http://lcs.dynamics.com/en/)\*                      | Obsahuje cloudový pracovní prostor spolupráce, který mohou použít odběratelé a jejich partneři ke správě projektů Dynamics 365 for Operations z předprodeje k implementaci a operacím. Tento web je užitečný ve všech fázích implementace. |
| [CustomerSource](http://www.customersource.com/)\*                       | Je hostitelem rozsáhlých zdrojů o školení a je primárním webem podpory pro aplikaci Dynamics 365 for Operations. Pro přístup k určitým zdrojům na tomto webu může být vyžadováno přihlášení.                                                                      |
| [Blog podpory](http://aka.ms/AXSupportBlog)                              | Obsahuje tipy a triky týmu podpory aplikace Dynamics 365 for Operations.                                                                                                                                                  |
| [MSDN](http://aka.ms/AXMSDN)                                             | Je hostitelem obsahu z předchozích verzí pro vývojáře.                                                                                                                                                                       |
| [TechNet](http://aka.ms/TechNet)                                         | Je hostitelem obsahu z předchozích verzí pro IT odborníky a uživatele aplikace.                                                                                                                                           |
| [Komunita Dynamics](http://community.dynamics.com/en/)                  | Je hostitelem blogů, fór a videí.                                                                                                                                                                                                           |
| [Microsoft.com/Dynamics/](http://www.microsoft.com/dynamics/)                 | Obsahuje hodnocení a informace o prodeji.                                                                                                                                                                                                 |



<a name="see-also"></a>Viz také
--------

[Systém nápovědy pro Dynamics 365 for Operations (seznam faktů ke stažení)](https://mbs.microsoft.com/files/public/CS/AX2012R3/DynamicsAXHelpSystemFactSheet.pdf)

[Záznamník úkolů v Microsoft Dynamics 365 for Operations](../user-interface/task-recorder.md)

[Vytváření dokumentace nebo školení pomocí záznamu úkolů](../user-interface/task-recorder.md)

[Noví nebo aktualizovaní Průvodci záznamem úloh (listopad 2016)](new-task-guides-november-2016.md)
[Noví nebo aktualizovaní Průvodci záznamem úloh (srpen 2016)](new-updated-task-guides-available-august-2016.md)
[Noví nebo aktualizovaní Průvodci záznamem úloh (květen 2016)](new-updated-task-guides-available-may-2016.md)
[Noví Průvodci záznamem úloh (únor 2016)](new-task-guides-available-february-2016.md)





