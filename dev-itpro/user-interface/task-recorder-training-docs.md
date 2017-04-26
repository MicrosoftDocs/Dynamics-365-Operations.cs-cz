---
title: "Vytváření dokumentace nebo školení pomocí záznamu úkolů"
description: "Toto téma vysvětluje, co Záznamník úkolů a úloh vodítka jsou, jak vytvořit úkol nahrávky a jak upravit úkol Microsoft provede a zahrnout je do vaši pomoc."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysHelpSetup
audience: Application User, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25391
ms.assetid: 59bf39f8-1464-441e-8b23-9a856c73471b
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: b21fd97426b331726c12ea29f89817a46dd445c3
ms.openlocfilehash: 38bce4a843f0db575c8d1ba08b7dc2ece8366663
ms.lasthandoff: 03/31/2017


---

# <a name="create-documentation-or-training-using-task-recordings"></a>Vytváření dokumentace nebo školení pomocí záznamu úkolů

[!include[banner](../includes/banner.md)]

Toto téma vysvětluje, co Záznamník úkolů a úloh vodítka jsou, jak vytvořit úkol nahrávky a jak upravit úkol Microsoft provede a zahrnout je do vaši pomoc.

<a name="learn-about-task-recorder"></a>Informace o Záznamníku úkolů
-------------------------

Záznamník úkolů je 365 Microsoft Dynamics pro operace nástroj, který slouží k záznamu akcí, které provádíte v uživatelském rozhraní (UI) produktu. Při použití Záznamníku úkolů jsou zaznamenány všechny události prováděné v uživatelském rozhraní, které jsou spouštěny na serveru, včetně přidání hodnot, změny nastavení a odebrání dat. Kroky, které zaznamenáte, jsou souhrnně označovány termínem *záznam úkolu*. Záznamy úloh lze používat mnoha způsoby:

-   **Záznamy úkolů lze přehrát jako průvodce úkolem.** Úloha vodítka jsou nedílnou část 365 Dynamics pomoci operací zkušenosti. Průvodce úkolu je řízené, s asistencí, interaktivní zkušeností kroky obchodního procesu. Uživatel obdrží pokyny k dokončení jednotlivých kroků pomocí je místních výzev (nebo "bublin"), která se zobrazí v uživatelském rozhraní a odkazují na prvek uživatelského rozhraní, který musí uživatel použít. "Bublin" obsahuje také informace o tom, jak pracovat s prvkem, jako je "Klepněte sem" nebo "Do tohoto pole zadejte hodnotu." Spustí Průvodce úkolu uživatele aktuální sadu dat a je uložena data, která je zadána v uživatelském prostředí.
-   **Záznamy úkolu může být zobrazen jako procesní úkony v podokně Nápověda.** Podokno Nápověda k hledání a zobrazit záznamy úkolu. Podokno Nápověda přístupná klepnutím na **?** Ikony v horním navigačním pruhu nebo můžete použít klávesové zkratky, **Ctrl + Shift +?**. Můžete číst kroky úkolu záznamu v podokně Nápověda, nebo můžete zvolit přehrát záznam jako vodítko úkolu tak, aby vás provede prostřednictvím uživatelského rozhraní.
-   **Záznamy úkolů lze uložit do BPM.** Záznam úkolu lze uložit na řádek hierarchie v knihovně modulu Modelování podnikových procesů (MPC) ve službě Lifecycle Services (LCS). Seznam kroků a vývojový diagram podnikového procesu bude vygenerován ze záznamu. Úloha nahrávek, které byly uloženy do knihovny BPM může být zobrazeno v 365 Dynamics pro operace jako Nápověda.
-   **Záznamy úkolů lze uložit jako dokumenty Word.** Tímto způsobem lze snadno vytvářet tisknutelné přepisy školení.

Můžete vytvořit úkol nahrávek, přehrávat nahrávky úloh poskytované společností Microsoft nebo upravit záznamy úloh poskytované společností Microsoft podle vaší konfigurace. Další informace o Záznamník úkolů naleznete v tématu [Záznamník úkolů v Dynamics 365 pro operace](task-recorder.md).

## <a name="plan-your-task-recording"></a>Plánování záznamu úkolů
Při vytváření nového záznamu úkolů nebo založení záznamu na záznamů úkolů Microsoft mějte na paměti následující informace.

-   Naplánujte záznam jako video. Proveďte všechna rozhodnutí dopředu.
-   Projděte si obchodní proces jednou nebo dvakrát bez záznamu, abyste se seznámili s jednotlivými kroky.
-   Při procházení procesu před záznamem si všimněte, kde se používají klávesové zkratky nebo klávesa **Enter**, abyste se vyhnuli jejich použití při skutečném záznamu.
-   Určete následující:
    -   Chcete seskupit kroky společně nebo do dílčích úkolů? Dílčí úkoly vizuální oddělují části procesu. Chcete-li například vytvořit záznam pro „vytváření a vydání produktu“, možná budete chtít seskupit kroky, které jsou nutné k vytvoření produktu, a poté seskupit kroky, které jsou nutné k vydání produktu. Dílčí úkoly také usnadňují čtení delších procesů.
    -   Opravdu chcete přidávat poznámky? A pokud ano, kam? Další informace najdete v tématu "Seznámení s různými typy poznámek".
    -   Jaké hodnoty přidáte do různých polí, jakmile dokončíte kroky obchodního procesu? Doporučujeme vědět, co vyberte nebo zadáte během procesu, abyste se nemuseli vracet zpět a opravovat chyby při vytváření záznamů.

**Zapište si popis a poznámky dopředu**

-   Na začátku každého záznamu úkolu je popis pole, které slouží k zadání úvodu k záznamu. Doporučujeme zapsat a uložit si popis předem do samostatného dokumentu, abyste jej mohli zkopírovat a vložit do záznamu úkolů při jeho nahrávání. Tímto způsobem se můžete věnovat úpravě textu, pokud nejste v procesu záznamu. Vyjmutí a vložení textu urychlí a zjednoduší proces záznamu.
-   Pro každý krok při záznamu úkolu můžete vytvořit poznámky. Během přehrávání průvodce úkolem se poznámky zobrazí v "bublině" jako poznámky nad nebo pod textem kroku. Při zobrazení jako text v podokně Nápověda, poznámky se zobrazí jako text vložený v kroku. Stejně jako v případě popisu doporučujeme zapsat a uložit poznámky do samostatného dokumentu. Při záznamu úkolu vyjměte a vložte poznámky z tohoto dokumentu.

**Seznámení s různými typy poznámek** Všechny poznámky jsou volitelné. Přidejte je, pouze když poskytují užitečné informace uživateli.

-   **Název**: název poznámky se zobrazí před text krok, který záznam úkolu automaticky generuje. V příručce úloh nadpis poznámky se zobrazí nad automaticky generovaný text. Použijte tento typ poznámek, chcete-li vysvětlit, proč uživatel provádí daný krok, nebo poskytnout další kontext.

Toto je podokno úprav, které se zobrazí při přidání poznámky během vytváření záznamu. Do pole **Nadpis** zadejte poznámku k nadpisu. 

[![screen1](./media/screen1.png)](./media/screen1.png) 

Toto je vzhled poznámky k nadpisu v bublině v průvodci záznamem úloh. 

[![– screen2](./media/screen2.png)](./media/screen2.png)

-   **Poznámky:** Poznámka k poznámkám se zobrazí za textem kroku, který Záznamník úkolů automaticky vygeneruje. V průvodci úkolem bude viditelná, pouze pokud uživatel klikne na odkaz **Zobrazit více** v bublině v průvodci úkolem. Použijte tento typ poznámky, chcete-li popsat cokoli, co musí uživatel znát pro dokončení kroku.

Toto je podokno úprav, které se zobrazí při přidání poznámky během vytváření záznamu. Do pole **Poznámky** zadejte poznámku k poznámkám. 

[![screen3](./media/screen3.png)](./media/screen3.png) 

To je vzhled poznámek poznámky do "bubliny" v příručce pro úkol.

[![screen4](./media/screen4.png)](./media/screen4.png)

-   **Informace o kroku**: tyto poznámky jsou vytvořeny klepnutím pravým tlačítkem myši na ovládací prvek, nebo kdekoli ve formuláři &lt;**Záznamník úkolů**&lt; ** krok přidat info. ** Informace o postupu se zobrazí jako očíslovaný krok v jakémkoli okamžiku vložení, přestože byla zaznamenána žádná akce v uživatelském rozhraní. Můžete přidat krok informací na úrovni formuláře nebo krok informací přidružený k ovládacímu prvku. Je-li krok informací přidružen k formuláři, zobrazí se "bublina" průvodce úkolem jinde ve formuláři, bez ukazatele, když je přehráván průvodce úkolem. Po o krok info je přidružen k ovládacímu prvku, Průvodce úkolu "bublin" bude přejděte ovládací prvek při přehrávání televize úkolu. V podokně Nápověda kroku anotaci info zobrazí jako očíslovaný krok s jakýkoli text zadán. Informace o postupu slouží k přípravě uživateli další kroky popisují kroky, které musí být provedeno mimo Dynamics 365 operací nebo odkazovat na jiné záznamy (i když hyperinks nelze vytvořit v poznámky.).

**Určete, jak dlouho budete záznam provádět**

-   Uživatel bude obecně číst nebo přehrávat záznam od začátku do konce, takže nekombinujte kroky nebo úkoly, které je lépe provádět samostatně.
-   Snažte se nevytvářet záznamy dlouhého scénáře, který zahrnuje více dílčích procesů. Například téma „Práce v oddělení služeb pro odběratele v obchodě“ je příliš široké. Rozdělte je na kratší úkoly, například „Přijmout vrácení“ a „Přidat k dárkovému poukazu“.
-   Pokud lze úkol provést v rámci několika různých obchodních procesů, vytvořte pro něj samostatný záznam. Můžete na něj odkázat v ostatních záznamech.
-   Pokud proces zahrnuje více úkolů, které osoba pravděpodobně provede najednou, lze úkoly uložit do jednoho záznamu, například "Nastavení a přiřazení profilů funkcí".
-   Pokud jde o něco, co uživatel udělá jednou (například konfigurace), a pak o další úkol, který může provést okamžitě po prvním, který se však provádí opakovaně a samotně, rozdělte je do dvou záznamů úkolů.

**Rozhodnout, pokud v uživatelském rozhraní, spuštění nahrávání** stránky, které jsou při spuštění nahrávání záznamu úkolu ovlivní stránky, která zobrazení úloh průvodce pro. Například pokud chcete úkol nahrávání uvedené v podokně Nápověda při kliknutí na tlačítko Nápověda na stránce parametry hlavní knihy, je nutné spustit nahrávání na stránce parametry hlavní knihy. **Uložte záznamy jako soubory AXT** Jakmile dokončíte vytvoření nebo úpravu záznamu úkolu, máte k dispozici několik možností pro stažení nebo uložení záznamu. Soubor lze stáhnout jako balíček záznamu úkolu (AXTR), jako neupravený soubor záznamu (XML) nebo jako dokument aplikace Word a uložit soubor do knihovny LCS. Je vhodné záznam úkolu vždy uložit jako souboru balíčku záznamu úkolů (AXTR). To vám usnadní údržbu souborů, pokud bude později nutné změnit postupy nebo poznámky. Chcete-li stáhnout soubor jako dokument aplikace Word, uložte jej také jako soubor balíčku záznamu úlohy.

## <a name="create-your-task-recording"></a>Vytvoření záznamu úkolu
Walk-through podrobný postup naleznete v tématu [jak vytvořit záznam úkolu](task-recorder.md).

## <a name="copy-and-customize-microsofts-task-recordings"></a>Kopírování a přizpůsobení záznamu úkolů společnosti Microsoft
Můžete stáhnout a upravit záznamy úloh společnosti Microsoft jejich použití pro dokumentaci nebo školicí materiály. Při stažení záznamu úkolu Microsoft postupujte takto:

1.  V 365 Dynamics pro operace otevřete záznam úkolu. Záznamník úkolů se nachází v nabídce **Nastavení**.
2.  V podokně Záznamník úkolů klikněte na tlačítko **Udržovat záznam.**
3.  V části **Kde je záznam** klikněte na tlačítko **Nachází se v knihovně LCS**.
4.  Klikněte na možnost **Vybrat knihovnu LCS**.
5.  Vyberte knihovnu Microsoft global.
6.  Ve stromovém zobrazení vyberte uzel knihovny obchodního procesu přidružený k záznamu úkolů.
7.  Klepněte na tlačítko **OK**.
8.  Klikněte na tlačítko **Spustit**.
9.  V tomto okamžiku kroku pomocí záznamu, změna jakékoli kroky průběžně jej znovu zaznamenat. **Poznámka:**: Chcete-li změnit text, nahrávání, můžete otevřít záznam v **úprava poznámky záznamu** režimu a potom jej uložte.
10. Po přehrání záznamu do konce klikněte na tlačítko **Zastavit** na panelu Záznamníku úkolů v horní části obrazovky.
11. Vyberte, jak chcete záznam úkolu uložit.

## <a name="include-your-task-recordings-in-the-help-pane"></a>Zahrnout úkol nahrávek v podokně Nápověda
Nahrávek vlastní úkol zobrazit v podokně Nápověda, tak, že mohou být přehrávána jako vodítka úkolů nebo zobrazit jako text, uložit do knihovny BPM nahrávek úkolu a potom aktualizujte parametry systému nápovědy přejděte do knihovny BPM. Další informace naleznete v tématu [připojit systém nápovědy.](../get-started/help-connect.md)

<a name="see-also"></a>Viz také
--------

[Nápověda k aplikaci Dynamics 365 pro operace](..\get-started\help-overview.md)

[Nápověda pro připojení](..\get-started\help-connect.md)

[Záznamník úkolů v Dynamics 365 pro operace](task-recorder.md)

[Nedávno přidané funkce Záznamník úkolů](\core\get-started\recently-added-editing-features-in-task-recorder)

[Vytvoření nové knihovny školení pro Dynamics AX v rámci poskytování služeb pomocí Záznamníku úkolů (externí odkaz)](https://docs.com/mufife/163372c6-f366-4c5a-94fa-93e2c25f878a/creating-new-training-libraries-for-dynamics-ax)

[Vytvořit témata nápovědy ve formátu RTF pomocí Záznamníku úkolů (externí odkaz)](https://mbspartner.microsoft.com/AX/Videos/970)




