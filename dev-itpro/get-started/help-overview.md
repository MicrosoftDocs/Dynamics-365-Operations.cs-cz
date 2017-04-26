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

-   Dokumentace sítě
-   Průvodci úkoly

Se dostanete články a úkol vodítka z podokna v 365 Dynamics pro operace jak je znázorněno v následujícím snímku obrazovky. [![Podokno Nápověda](./media/help-pane-ops-task-guides-1024x741.png)](./media/help-pane-ops-task-guides.png) Tento článek popisuje systém nápovědy a vysvětluje, jak vytvořit vlastní dokumentaci a školicí prostředky pro vaši organizaci.

## <a name="help-on-docsmicrosoftcom"></a>Nápověda k docs.microsoft.com
Na webu docs.microsoft.com ([docs.microsoft.com/dynamics365/operations](https://docs.microsoft.com/en-us/dynamics365/#pivot=solutions&panel=solutions_operations) je primárním zdrojem dokumentaci produktu Dynamics 365 pro operace. Web nabízí následující funkce:

-   **Přístup k aktuální obsah** – web nám rychlejší a pružnější způsob, jak vytvořit, zaujme a aktualizovat dokumentaci k produktu. Díky tomu pomáhá zajistit, že budete mít přístup k aktuálním technickým informacím.
-    **Obsah, který je zapsán odborníky** – tento web poskytuje rozsáhlejší sadu dokumentace, která může být zvýšena členové komunity i mimo společnost Microsoft.
-   ** Přístup k různým typům obsahu ** – web umožňuje rychlý přístup různých typů obsahu o 365 Dynamics pro operace, například prezentace Microsoft Office Mix, úkol vodítka, videa a články wiki.
-    **Obsah, který podporuje obchodní procesy** – web obsahuje obchodní proces – zaměřený obsah využívá z modelování obchodních procesů (BPM) v Microsoft Dynamics Lifecycle Services (LCS).

Jsme jste přeneseni veškerý obsah z naší předchozí nápovědy wiki do dokumentů. Jsme náš nový web a Doufám, že bude příliš, velmi těší.

### <a name="when-can-we-use-it"></a>Jak ji můžeme používat?

Čtení obsahu v docs nyní – je plně veřejné a s možností vyhledávání bez nutnosti přihlášení. K hledání obsahu můžete použít kterýkoli svůj oblíbený vyhledávač. Články na webu můžete komentovat, pokud vyberete po přihlášení účtu GitHub.


## <a name="task-guides"></a>Průvodci úkoly
Průvodce úkolu je řízené, s asistencí, interaktivní prezentaci, která vás provede kroky úkolu nebo obchodního procesu. Z podokna můžete otevřít Průvodce úkolu (play). Nejprve na tlačítko guide úkol, podokno Nápověda se zobrazí podrobné pokyny pro daný úkol. Lokalizované úkol vodítka jsou nyní k dispozici. [![Průvodce úkolu zobrazení pro čtení](./media/task-guide-ops-1024x742.png)](./media/task-guide-ops.png) začít zkušenosti s asistencí, interaktivní, klepněte na tlačítko **startem úlohy** v dolní části podokna Nápověda. Černá ukazatel otevře a určuje akci, kterou je třeba provést. Postupujte podle pokynů v uživatelském rozhraní a zadejte data podle pokynů. [![Instrukce krok průvodce úkolu](./media/task-guide-step-1-ops.png)](./media/task-guide-step-1-ops.png)**důležité:** je skutečná data, která zadáte při hraní úloh průvodce. Pokud jste ve výrobním prostředí, budou zadána data, která skutečně používáte.

### <a name="it-all-begins-with-task-recorder"></a>Vše začíná v Záznamníku úkolů

Průvodci úkolem se vytvoří pomocí Záznamníku úkolů. Při použití Záznamníku úkolů jsou zaznamenány všechny akce, které provedete v uživatelském rozhraní aplikace Dynamics 365 for Operations (například kliknutí na nabídky, změna nastavení a zadávání dat). Kroky, které zaznamenáte, jsou souhrnně označovány termínem záznam úkolu. Jak jsme vysvětlili v předchozím oddílu, lze zobrazit záznamy úloh v podokně Nápověda a přehrát jako průvodce úkolem. Existují však další možnosti, jak lze použít záznamy úloh:

-   **Uložení záznamu úkolu do BPM** – Lze uložit záznam úkolu na řádek v hierarchii knihovny BPM ve službě LCS. Při uložení záznamu úkol do BPM bude vygenerován vývojový diagram společně s kroky záznamu. **Poznámka:** Chcete-li zobrazit záznam úkolu v podokně Nápověda aplikace Dynamics 365 for Operations a přehrát jej jako průvodce úkolem, musíte záznam uložit do knihovny BPM.
-   **Uložení záznamů úkolů jako jako dokumentů Word** – Uložením záznamu úkolu jako dokumentu aplikace Microsoft Word můžete snadno vytvářet tisknutelné přepisy školení pro vaši organizaci.

Další informace o Záznamník úkolů naleznete v tématu [Záznamník úkolů v Dynamics 365 pro operace](../user-interface/task-recorder.md).

### <a name="creating-customized-task-recordings"></a>Vytvoření přizpůsobených záznamů úkolů

Můžete vytvořit vlastní záznamy úkolů nebo můžete stáhnout a upravit záznam úkolu, který poskytuje společnost Microsoft. Proto můžete vytvořit upravenou nápovědu pro vaši organizaci, které odpovídá konkrétní implementaci aplikace Dynamics 365 for Operations. Zobrazit úkol v 365 Dynamics pro podokno Nápověda operace nahrávání a hrát jako vodítko úkolu, budete muset uložit do knihovny BPM v LCS nahrávání. Pokud jste s partnerem a podporu knihovny do knihovny pro podnikové a zahrnout do řešení, je k dispozici zákazníkům. Úplné pokyny naleznete v tématu [použití úkolu nahrávky k vytvoření dokumentace nebo školení](../user-interface/task-recorder.md).

## <a name="in-product-help"></a>Nápověda v produktu
Chcete-li získat přístup k obsahu nápovědy v rámci Dynamics 365 pro operace, **pomoci** (**?**) ikonu a potom zvolte Nápověda nebo stiskněte kombinaci kláves Ctrl + Shift +?. V obou případech se otevře podokno Nápověda. Z podokna můžete přistupovat články nebo úkol vodítka. [![](./media/help-pane-wiki-1024x684.png)](./media/help-pane-wiki.png)

### <a name="accessing-articles-from-the-help-pane"></a>Přístup z podokna články

Články, které se vztahují na 365 Dynamics pro operace klienta můžete přistupovat z podokna nápovědy. Při prvním otevření podokna nápovědy a klepněte na tlačítko **Wiki** kartu, zobrazí se články, které platí pro stránky, který jste právě na v 365 Dynamics pro operace. Pokud jsou nalezeny žádné články, můžete zadat klíčová slova pro upřesnění hledání. Klepnutím na článek v podokně Nápověda na nové záložce otevře v prohlížeči a zobrazí v článku. 

### <a name="accessing-task-guides-from-the-help-pane"></a>Přístup z podokna úloh vodítka

Předtím, než se dostanete z podokna úloh vodítka, správce systému musí přejít **parametry systému** stránce 365 Dynamics pro operace a konfiguraci některých nastavení. **Poznámky:**

-   Než bude možné konfigurovat nápovědu, musíte být přihlášeni pomocí účtu ve stejném klientovi, jako ve kterém je aplikace Dynamics 365 for Operations nasazena.
-   Není možné připojit se do knihovny LCS z instance aplikace Dynamics 365 for Operations spuštěné na místním virtuálním pevném disku (VHD).

[![Formulář Parametry systému nápovědy nastavení](./media/system-parameters_ops-1024x437.png)](./media/system-parameters_ops.png) na **parametry systému** stránky, postupujte takto:

1.  **Upozornění: **při prvním otevření karty Nápověda je nutné se připojit ke Lifecycle Services. Ujistěte se, klepněte na odkaz doprostřed formuláře, čekání na připojení, zavřete dialogové okno a klepněte na tlačítko OK, chcete-li získat parametry formuláře. [![Připojit k LCS](./media/connect-to-lcs-crop-1024x365.png)](./media/connect-to-lcs-crop.png)
2.  Vyberte projekt služby Lifecycle Services pro připojení.
3.  Vyberte knihovny BPM (v rámci vybraného projektu), ze kterých chcete načíst záznamy úkolů.
4.  Nastavte pořadí zobrazení knihoven BPM. Tato možnost určuje pořadí, ve kterém se záznamy úkolů z knihoven zobrazí v podokně Nápověda.

Jakmile správce systému provede tyto kroky, můžete otevřít podokno Nápověda a kliknout na kartu **Průvodci úkolem**. Nyní uvidíte úkol vodítka, které platí pro stránky, který jste právě na v 365 Dynamics pro operace. Pokud jsou nalezeny žádné vodítka úkolu, můžete zadat klíčová slova pro upřesnění hledání. Po klepnutí na úlohu televize v podokně Nápověda podokna nápovědy jsou uvedeny podrobné pokyny a hrajete úloh průvodce. [![Průvodce úkolu zobrazení pro čtení](./media/task-guide-ops-1024x742.png)](./media/task-guide-ops.png)

### <a name="where-are-the-translated-task-guides"></a>Kde jsou přeložený vodítka úkol?

Vodítka jsou vydány v knihovnách s "Všechny jazyky" v názvu úkolu přeložit. V 365 Dynamics pro operace lokalizované příručku úloh Nápověda Přesvědčte se, zda jste připojeni do knihovny apppropriate. Jazyk, ve kterém průvodce úkolu se zobrazí v je řízen pro každého uživatele jazykové nastavení v části **možnosti**&gt;**Předvolby**. 
-   Pokud Průvodce úkolu byl přeložen, při otevření této úlohy vodítko, které všechny text příručky pro úlohy se zobrazí ve vybraném jazyce.
-   Pokud Průvodce úlohy nebyly dosud přeloženy, po jejím otevření, zobrazí se pouze část textu (text ovládacích prvků) ve vybraném jazyce.

## <a name="additional-resources"></a>Další prostředky
V následující tabulce jsou uvedeny weby, které poskytují obsah aplikace Dynamics 365 for Operations. Naše weby s obsahem jsou uspořádány pro podporu cyklu odběratele. Každá fáze je podporována jinou sadou webu. Servery, na kterých je uvedena hvězdička (\*) u názvu vyžadují, abyste se přihlásili pomocí účtu, který je přidružen servisního plánu.

| Pracoviště                                                                     | popis                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Docs.microsoft.com](https://docs.microsoft.com/en-us/dynamics365/#pivot=solutions&panel=solutions_operations) | Hostitelé nebo odkazy na veškerou dokumentaci k produktům pro aplikaci Dynamics 365 for Operations.                                                                                                                                                               |
| [Lifecycle Services](http://lcs.dynamics.com/en/)\*                      | Obsahuje cloudový pracovní prostor spolupráce, který mohou použít odběratelé a jejich partneři ke správě projektů Dynamics 365 for Operations z předprodeje k implementaci a operacím. Tento web je užitečný ve všech fázích implementace. |
| [CustomerSource](http://www.customersource.com/)\*                       | Je hostitelem rozsáhlých zdrojů o školení a je primárním webem podpory pro aplikaci Dynamics 365 for Operations. Pro přístup k určitým zdrojům na tomto webu může být vyžadováno přihlášení.                                                                      |
| [Podpora blogu](http://aka.ms/AXSupportBlog)                              | Obsahuje tipy a triky týmu podpory aplikace Dynamics 365 for Operations.                                                                                                                                                  |
| [MSDN](http://aka.ms/AXMSDN)                                             | Je hostitelem obsahu z předchozích verzí pro vývojáře.                                                                                                                                                                       |
| [TechNet](http://aka.ms/TechNet)                                         | Je hostitelem obsahu z předchozích verzí pro IT odborníky a uživatele aplikace.                                                                                                                                           |
| [Dynamics Společenství](http://community.dynamics.com/en/)                  | Je hostitelem blogů, fór a videí.                                                                                                                                                                                                           |
| [Microsoft.com/Dynamics/](http://www.microsoft.com/dynamics/)                 | Obsahuje hodnocení a informace o prodeji.                                                                                                                                                                                                 |



<a name="see-also"></a>Viz také
--------

[Nápovědy Dynamics 365 pro operace systému (ke stažení fakt listů)](https://mbs.microsoft.com/files/public/CS/AX2012R3/DynamicsAXHelpSystemFactSheet.pdf)

[Záznamník úkolů v aplikaci Microsoft Dynamics 365 pro operace](../user-interface/task-recorder.md)

[Vytváření dokumentace nebo školení pomocí záznamu úkolů](../user-interface/task-recorder.md)

[Nové nebo aktualizované úkoly provede (listopad 2016)](new-task-guides-november-2016.md)<ph id="t1">
</ph>[nového nebo aktualizovaného úkolu provede (srpen 2016)](new-updated-task-guides-available-august-2016.md)<ph id="t2">
</ph>[nového nebo aktualizovaného úkolu provede (květen 2016)](new-updated-task-guides-available-may-2016.md)<ph id="t3">
</ph>[nový úkol provede (únor 2016)](new-task-guides-available-february-2016.md)






