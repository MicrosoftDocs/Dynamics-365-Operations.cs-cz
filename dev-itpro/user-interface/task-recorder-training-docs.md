---
title: "Vytváření dokumentace nebo školení pomocí záznamu úkolů"
description: "Toto téma vysvětluje, co je Záznamník úkolů a průvodci záznamem úloh, jak vytvořit nahrávky úkolů a jak přizpůsobit průvodce záznamem úloh Microsoft a zahrnout je do nápovědy."
author: josaw1
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: SysHelpSetup
audience: Application User, IT Pro
ms.reviewer: annbe
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 25391
ms.assetid: 59bf39f8-1464-441e-8b23-9a856c73471b
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 529751c09b8f99f986cad23a633bea661929d558
ms.openlocfilehash: d5e4857081134808b194d3248dd8739f83b57d6e
ms.contentlocale: cs-cz
ms.lasthandoff: 08/09/2017

---

# <a name="create-documentation-or-training-using-task-recordings"></a>Vytváření dokumentace nebo školení pomocí záznamu úkolů

[!include[banner](../includes/banner.md)]

Toto téma vysvětluje, co je Záznamník úkolů a průvodci záznamem úloh, jak vytvořit nahrávky úkolů a jak přizpůsobit průvodce záznamem úloh Microsoft a zahrnout je do nápovědy.

> [!IMPORTANT]
> Nelze vytvořit vlastní průvodce záznamem úloh pro aplikaci Dynamics 365 for Talent. Systém nápovědy pro aplikaci Talent se automaticky připojí k průvodcům záznamem úloh pro produkt. 

<a name="learn-about-task-recorder"></a>Informace o Záznamníku úkolů
-------------------------

Záznamník úkolů je nástroj aplikace Dynamics AX, který umožňuje zaznamenat akce prováděné v uživatelském rozhraní produktu. Při použití Záznamníku úkolů jsou zaznamenány všechny události prováděné v uživatelském rozhraní, které jsou spouštěny na serveru, včetně přidání hodnot, změny nastavení a odebrání dat. Kroky, které zaznamenáte, jsou souhrnně označovány termínem *záznam úkolu*. Záznamy úloh lze používat mnoha způsoby:

-   **Záznamy úkolů lze přehrát jako průvodce úkolem.** Průvodci záznamem úloh jsou nedílnou součástí prostředí nápovědy. Průvodce záznamem úloh je kontrolovaný, řízený a interaktivní způsob, který vás provede kroky daného úkolu nebo obchodního procesu. Uživatel obdrží pokyny k dokončení jednotlivých kroků pomocí je místních výzev (nebo "bublin"), která se zobrazí v uživatelském rozhraní a odkazují na prvek uživatelského rozhraní, který musí uživatel použít. Bublina obsahuje také informace o tom, jak pracovat s prvkem, jako je "Klepněte sem" nebo "Do tohoto pole zadejte hodnotu." Spouští se v rámci aktuální datové sady uživatele a dat, která jsou zadána a uložena v prostředí uživatele.
-   **Záznamy úloh lze zobrazit jako kroky postupu v podokně nápovědy.** Podokno nápovědy lze použít k hledání a zobrazení záznamů úloh. Do podokna Nápověda můžete přejít kliknutím na ikonu **?** v horním navigačním pruhu nebo můžete použít klávesové zkratky, **Ctrl + Shift +?**. Kroky záznamu úkolu si můžete přečíst v podokně nápovědy nebo můžete zvolit přehrání záznamu jako průvodce úkolem, který vás provede uživatelským rozhraním.
-   **Záznamy úkolů lze uložit do BPM.** Záznam úkolu lze uložit na řádek hierarchie v knihovně modulu Modelování podnikových procesů (MPC) ve službě Lifecycle Services (LCS). Seznam kroků a vývojový diagram podnikového procesu bude vygenerován ze záznamu. Záznamníky úkolů, které byly uloženy do knihovny BPM, lze zobrazit jako nápovědu.
-   **Záznamy úkolů lze uložit jako dokumenty Word.** Tímto způsobem lze snadno vytvářet tisknutelné přepisy školení.

Můžete vytvořit vlastní záznamy úkolů, přehrávat záznamy úkolů poskytované společností Microsoft nebo upravovat záznamy úkolů poskytované společností Microsoft podle konfigurace. Další informace o Záznamníku úkolů naleznete v tématu [Záznamník úloh](task-recorder.md).

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
-   Pro každý krok při záznamu úkolu můžete vytvořit poznámky. Během přehrávání průvodce úkolem se poznámky zobrazí v "bublině" jako poznámky nad nebo pod textem kroku. Při prohlížení jako textu v podokně nápovědy se poznámky zobrazí jako text vložený v kroku. Stejně jako v případě popisu doporučujeme zapsat a uložit poznámky do samostatného dokumentu. Při záznamu úkolu vyjměte a vložte poznámky z tohoto dokumentu.

**Seznámení s různými typy poznámek** Všechny poznámky jsou volitelné. Přidejte je, pouze když poskytují užitečné informace uživateli.

-   **Nadpis:** Poznámka k nadpisu se zobrazí za textem kroku, který Záznamník úkolů automaticky vygeneruje. V průvodci záznamem úloh se nadpis poznámky zobrazí nad automaticky generovaným textem. Použijte tento typ poznámek, chcete-li vysvětlit, proč uživatel provádí daný krok, nebo poskytnout další kontext.

Toto je podokno úprav, které se zobrazí při přidání poznámky během vytváření záznamu. Do pole **Nadpis** zadejte poznámku k nadpisu. 

[![screen1](./media/screen1.png)](./media/screen1.png) 

Toto je vzhled poznámky k nadpisu v bublině v průvodci záznamem úloh. 

[![screen2](./media/screen2.png)](./media/screen2.png)

-   **Poznámky:** Poznámka k poznámkám se zobrazí za textem kroku, který Záznamník úkolů automaticky vygeneruje. V průvodci úkolem bude viditelná, pouze pokud uživatel klikne na odkaz **Zobrazit více** v bublině v průvodci úkolem. Použijte tento typ poznámky, chcete-li popsat cokoli, co musí uživatel znát pro dokončení kroku.

Toto je podokno úprav, které se zobrazí při přidání poznámky během vytváření záznamu. Do pole **Poznámky** zadejte poznámku k poznámkám. 

[![screen3](./media/screen3.png)](./media/screen3.png) 

Toto je vzhled poznámky v bublině v průvodci záznamem úloh.

[![screen4](./media/screen4.png)](./media/screen4.png)

-   **Krok Informace**: Tyto poznámky se vytvářejí kliknutím pravým tlačítkem na ovládací prvek nebo na libovolné místo ve formuláři &lt; **Záznamník úloh** &lt; **Přidat informační krok. **Informační kroky se zobrazují v jakémkoli kroku vložení, i když nebyla zaznamenána žádná akce v uživatelském rozhraní. Můžete přidat krok informací na úrovni formuláře nebo krok informací přidružený k ovládacímu prvku. Je-li krok informací přidružen k formuláři, zobrazí se "bublina" průvodce úkolem jinde ve formuláři, bez ukazatele, když je přehráván průvodce úkolem. Je-li informační krok přidružen k formuláři, bude "bublina" průvodce záznamem úloh odkazovat na ovládací prvek, kde se průvodce záznamem úloh přehrává. V podokně Nápověda se poznámka informačního kroku zobrazuje jako očíslovaný krok s jakýmkoli zadaným textem. Kroky informací slouží k přípravě uživatele na následující kroky, k popisu kroků, které je třeba provést mimo aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, nebo pro účely odkazování na jiné záznamy (i když v poznámkách nelze vytvořit hypertextové odkazy).

**Určete, jak dlouho budete záznam provádět**

-   Uživatel bude obecně číst nebo přehrávat záznam od začátku do konce, takže nekombinujte kroky nebo úkoly, které je lépe provádět samostatně.
-   Snažte se nevytvářet záznamy dlouhého scénáře, který zahrnuje více dílčích procesů. Například téma „Práce v oddělení služeb pro odběratele v obchodě“ je příliš široké. Rozdělte je na kratší úkoly, například „Přijmout vrácení“ a „Přidat k dárkovému poukazu“.
-   Pokud lze úkol provést v rámci několika různých obchodních procesů, vytvořte pro něj samostatný záznam. Můžete na něj odkázat v ostatních záznamech.
-   Pokud proces zahrnuje více úkolů, které osoba pravděpodobně provede najednou, lze úkoly uložit do jednoho záznamu, například "Nastavení a přiřazení profilů funkcí".
-   Pokud jde o něco, co uživatel udělá jednou (například konfigurace), a pak o další úkol, který může provést okamžitě po prvním, který se však provádí opakovaně a samotně, rozdělte je do dvou záznamů úkolů.

**Rozhodněte, kde v uživatelském rozhraní spustit nahrávání** Stránka, na kterou přejdete při spuštění nahrávání záznamu úkolu, ovlivní, pro kterou stránku se průvodce záznamem úloh přehraje. Například pokud chcete uvést záznam úlohy v podokně Nápověda při kliknutí na tlačítko Nápověda na stránce Parametry hlavní knihy, je nutné spustit nahrávání na stránce parametry hlavní knihy. **Uložte záznamy jako soubory AXT** Jakmile dokončíte vytvoření nebo úpravu záznamu úkolu, máte k dispozici několik možností pro stažení nebo uložení záznamu. Soubor lze stáhnout jako balíček záznamu úkolu (AXTR), jako neupravený soubor záznamu (XML) nebo jako dokument aplikace Word a uložit soubor do knihovny LCS. Je vhodné záznam úkolu vždy uložit jako souboru balíčku záznamu úkolů (AXTR). To vám usnadní údržbu souborů, pokud bude později nutné změnit postupy nebo poznámky. Chcete-li stáhnout soubor jako dokument aplikace Word, uložte jej také jako soubor balíčku záznamu úlohy.

## <a name="create-your-task-recording"></a>Vytvoření záznamu úkolu
Podrobný přehled kroků naleznete v tématu [Vytvoření záznamu úkolu](task-recorder.md).

## <a name="copy-and-customize-microsofts-task-recordings"></a>Kopírování a přizpůsobení záznamu úkolů společnosti Microsoft
Můžete stáhnout a upravovat záznamy úkolů společnosti Microsoft a použít je pro vlastní dokumentaci k nápovědě nebo výukové materiály. Při stažení záznamu úkolu Microsoft postupujte takto:

1.  Otevřete záznamník úloh. Záznamník úkolů se nachází v nabídce **Nastavení**.
2.  V podokně Záznamník úkolů klikněte na tlačítko **Udržovat záznam.**
3.  V části **Kde je záznam** klikněte na tlačítko **Nachází se v knihovně LCS**.
4.  Klikněte na možnost **Vybrat knihovnu LCS**.
5.  Vyberte globální knihovnu Microsoft.
6.  Ve stromovém zobrazení vyberte uzel knihovny obchodního procesu přidružený k záznamu úkolů.
7.  Klepněte na tlačítko **OK**.
8.  Klikněte na tlačítko **Spustit**.
9.  V tomto okamžiku procházejte záznam a změňte jakékoli kroky v průběhu nahrávání.. **Poznámka:**: Chcete-li pouze změnit text nahrávání, můžete otevřít záznam v režimu **úprava poznámky záznamu** režimu a potom ho uložit.
10. Po přehrání záznamu do konce klikněte na tlačítko **Zastavit** na panelu Záznamníku úkolů v horní části obrazovky.
11. Vyberte, jak chcete záznam úkolu uložit.

## <a name="include-your-task-recordings-in-the-help-pane"></a>Zahrnutí záznamu úkolu do podokna nápovědy
Chcete-li zobrazovat vlastní záznamy úkolů v podokně nápovědy, aby je bylo možné přehrát jako průvodce úkolem nebo zobrazit jako text, je třeba záznamy úkolů uložit do vlastní knihovny BPM a poté aktualizovat systémové parametry nápovědy tak, aby odkazovaly na knihovnu BPM. Další informace naleznete v tématu [Připojení systému nápovědy](../get-started/help-connect.md).

<a name="see-also"></a>Viz také
--------

[Přehled nápovědy](..\get-started\help-overview.md)

[Připojení nápovědy](..\get-started\help-connect.md)

[Záznamník úkolů](task-recorder.md)

[Vytvořit témata nápovědy ve formátu RTF pomocí Záznamníku úkolů (externí odkaz)](https://mbspartner.microsoft.com/AX/Videos/970)

